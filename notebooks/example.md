# <div dir="rtl">الوصول إلى بيانات MERRA-2 في السحابة</div>

```python
import earthaccess
import xarray as xr
from matplotlib import pyplot

auth = earthaccess.login()
```

<div dir="rtl">
## استخدام `earthaccess`
</div>

<div dir="rtl">
قمنا في الدرس السابق بتنزيل ملف netCDF4 يدوياً من محرك البحث Earthdata Search التابع لوكالة لناسا. لنرى الآن كيف يمكننااستخدام كود بايثون  Python بدلاً من ذلك لتنزيل البيانات من السحابة.

يمكن استخدام مكتبة `earthaccess` لبحث البيانات وتنزيلها من محرك البحث Earthdata Search دون فتح متصفح الويب والنقر هنا وهناك. بالنسبة لبعض التطبيقات، تتيح لنا هذه الخاصية لنا كتابة كود بايثون أكثر شفافية وقابلية للتكرار، لأنها تسمح لأي شخص بالحصول على نفس البيانات الخام التي بدأنا بها بسهولة.

نستخدم `()earthaccess.search_data` للحصول على **جزيئة** واحدة أو أكثر توافق استعلام بحث ما. الجزيئة هي مجموعة مفردة من البيانات المرتبطة بمهمة أو منتج معين يخص لوكالة لناسا.

**هل تتذكر أين يوجد الاسم المختصر لمنتجات Earthdata؟** ستجده في موقعين من صفحة المعلومات(i) :

![](./assets/M1_screenshot_Earthdata_Search_MERRA2_info.png)

**نستخدم الاسم المختصر `short_name` للإشارة إلى طائفة من جزيئات البيانات التي نرغب في البحث عنها.**

نجد في هذا المثال أن هناك 32 جزيئة بيانات بين 1 مايو و1 يونيو، ضمناً.
</div>


```python
results = earthaccess.search_data(
    short_name = 'M2SDNXSLV',
    temporal = ("2023-05", "2023-06"))
results[0]
```

<div dir="rtl">
لم يتم تنزيل أي بيانات حتى الآن؛ لدينا فقط مرجع للبيانات المخزنة في السحابة.
</div>


```python
type(results[0])
```

<div dir="rtl">
لتنزيل جزيئة، يمكننا استخدام `()earthaccess.open`.

#### &#x1F6A9; <span style="color:red">انتبه جيداً</span>

** من المهم الإشارة إلى أن `()earthaccess.open` يتطلب *تسلسلاً* من الجزيئات لفتحه.** لذلك، حتى لو كنا نرغب في فتح جزيئة واحدة فقط، ينبغي تقديم هذه الجزيئة كجزء من قائمة أو مجموعة في بايثون.
</div>


```python
files = earthaccess.open(results[0:2]) # ملاحظة: open() يتطلب تسلسلاً من مراجع الملفات
```


```python
type(files[0])
```

<div dir="rtl">
تم تنزيل الجزئيات في ذاكرة الكمبيوتر الخاص بنا. لفتح أحد الملفات التي تم تنزيلها في بايثون ، نستخدم الآن `xarray`. يحدث تأخير طفيف عند استخدام `()open_dataset` على جزيئة تم تنزيلها باستخدام `()earthaccess.open` لأن على `xarray` تحليل الملف وتحديد نظام الإحداثيات والأبعاد.
</div>


```python
ds2 = xr.open_dataset(files[0])
ds2
```

<div dir="rtl">
مجموعة بيانات `xarray.Dataset` الناتجة جاهزة للرسم!
</div>


```python
ds2['T2MMIN'].plot()
```

## <div dir="rtl">الحصول على سلسلة زمنية لدرجات الحرارة</div>


<div dir="rtl">
لقد عمل هذا بشكل رائع مع ملف واحد، ولكن ماذا لو أردنا إنشاء سلسلة زمنية من بيانات المناخ؟ نعلم أن مجموعات بيانات `xarray` يمكن أن تحتوي على بُعد زمني، مما يجعلها قادرة على تمثيل أكثر من حالة واحدة في الزمن. كيف يمكننا إنشاء مجموعة بيانات كهذه؟

في المثال التالي، سنستخدم حلقة `for`  لإجراء تكرار عبر جزيئات  MERRA-2، وفتح كل منها ثم اختيار قيمة `T2MMIN` (درجة الحرارة الدنيا) في موقع محدد. نضيف هذه القيمة إلى قائمة ما، إلى جانب تاريخ (`"time"`) الجزئية، لبناء مجموعة بيانات السلسلة الزمنية.
</div>


```python
results = earthaccess.search_data(
    # ملاحظة: قد يستغرق هذا المثال نصف دقيقة باستخدام شبكة إنترنت جيدة.
    short_name = 'M2SDNXSLV',
    temporal = ("2023-05", "2023-06"))

time_list = []
data_list = []
file_list = earthaccess.open(results)
for filename in file_list:
    ds = xr.open_dataset(filename)
    data_list.append(ds['T2MMIN'].sel(lat = 36.5, lon = 3.125).values)
    time_list.append(ds['T2MMIN']['time'].values)
```

<div dir="rtl">
لدينا الآن قائمة`list` بايثون تحتوي على قيم درجات الحرارة الدنيا وقائمة `list` أخرى بالتواريخ. أدناه، نرسم هذه البيانات بيانياً باستخدام `numpy` من أجل تحويل بيانات درجات الحرارة من كلفن (K) إلى الدرجة المئوية (C).
</div>


```python
import numpy as np

# التحويل من كلفن إلى الدرجة المئوية
data = np.array(data_list).ravel() - 273.15
time = np.array(time_list).ravel()

pyplot.figure(figsize = (12, 4))
pyplot.plot(time, data)
pyplot.ylabel('درجة الحرارة الدنيا (°C)')
```
