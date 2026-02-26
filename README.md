<div dir="rtl" style="direction: rtl; unicode-bidi: isolate; text-align: right;">

<p style="text-align: right;">
<a href="https://doi.org/10.5281/zenodo.18793037"><img src="https://zenodo.org/badge/1154837584.svg" alt="DOI"></a>
</p>

<h1 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
الوحدة 1: بيانات المناخ المفتوحة
</h1>

<blockquote style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
كيف تُستخدم أقمار ناسا الصناعية، والبيانات الحقلية، والنماذج لتشخيص نظام مناخ الأرض والتنبؤ به؟
وكيف يتم قياس التقلّبات المناخية ونمذجتها؟
</blockquote>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
تركّز الوحدة الأولى من
<a dir="ltr" href="https://openclimatescience.github.io/curriculum">منهج علوم المناخ المفتوحة</a>
على تعريف المتعلّمين بمنصة
<span dir="ltr">NASA Earthdata Search</span>
وبالتنوّع الكبير في مجموعات بيانات المناخ التي توفّرها ناسا.
<strong>وبنهاية هذه الوحدة، يُفترض أن تكون قادرًا على:</strong>
</p>

<ul style="direction: rtl; unicode-bidi: plaintext; text-align: right; list-style-position: inside;">
  <li>
    فهم كيفية توليد بيانات المناخ من مجموعات بيانات إعادة التحليل،
    ونماذج الدوران العامة،
    ونماذج نظام الأرض،
    ومعرفة أوجه الاختلاف بين هذه النماذج.
  </li>
  <li>
    معرفة أين يمكن الحصول على المتغيّرات المناخية المختلفة
    (مثل الهطول ودرجة الحرارة)
    عند المقاييس المكانية والزمانية المناسبة.
  </li>
  <li>
    إظهار القدرة على استخدام متغيّرات مناخية متعددة
    من مجموعات بيانات مناخية مختلفة.
  </li>
</ul>

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
المحتويات
</h2>

<ol dir="rtl" style="direction: rtl; unicode-bidi: plaintext; text-align: right; list-style-position: inside;">
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/01_Sources_of_Climate_Data.ipynb">
      مصادر بيانات المناخ
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/02_Intro_to_NASA_Earthdata_Search.ipynb">
      مقدمة إلى منصة <span dir="ltr">NASA Earthdata Search</span> وبيانات إعادة التحليل
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/03_Reading_MERRA2_Gridded_Climate_Data.ipynb">
      قراءة بيانات المناخ الشبكية <span dir="ltr">MERRA-2</span>
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/04_Accessing_MERRA2_Data_in_the_Cloud.ipynb">
      الوصول إلى بيانات <span dir="ltr">MERRA-2</span> عبر الحوسبة السحابية
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/05_Earth_Observation_Data.ipynb">
      مقدمة إلى بيانات رصد الأرض
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/06_Climate_Models.ipynb">
      مقدمة إلى نماذج المناخ
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/07_Using_Re-analysis_Data_to_Study_Drought.ipynb">
      استخدام بيانات إعادة التحليل لدراسة الجفاف
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/08_Using_NASA_Earth_Observations.ipynb">
      استخدام بيانات رصد الأرض من ناسا
    </a>
  </li>
</ol>

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
البدء
</h2>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
<span style="direction: rtl;">
اطّلع على دليل التثبيت
</span>
<a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/HOW_TO_INSTALL.md">
هنا
</a>.
</p>
<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
يمكنك تشغيل دفاتر
<span dir="ltr">Jupyter</span>
في هذا المستودع باستخدام
<a dir="ltr" href="https://docs.github.com/en/codespaces/overview">Github Codespaces</a>
أو باستخدام
<a dir="ltr" href="https://code.visualstudio.com/docs/devcontainers/containers">حاوية تطوير VSCode</a>.
وبعد تشغيل الحاوية، شغّل Jupyter Notebook عبر:
</p>

<div dir="ltr" style="unicode-bidi: isolate; text-align: left;">

  ```sh
# أنشئ كلمة المرور الخاصة بك عند الطلب
jupyter server password

# ثم شغّل Jupyter Notebook؛ وأدخل كلمة المرور عند الطلب
jupyter notebook

```

<div dir="rtl" style="direction: rtl; unicode-bidi: isolate; text-align: right;">

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
مخرجات التعلّم
</h2>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
تغطي هذه الدورة الكفاءات الأساسية التالية في
<a dir="ltr" href="https://github.com/OpenClimateScience/Core-Competencies/blob/main/ScienceCore-Competencies.md">
<span dir="ltr">Core Competencies in Computational Data Science</span>
</a>:
</p>

<ul style="direction: rtl; unicode-bidi: plaintext; text-align: right; list-style-position: inside;">
  <li>
    تُحفظ البيانات الخام دون تعديل وبمعزل عن أي مشتقات معالجة أو نتائج تحليل.
    (<span dir="ltr">CC1.1</span>)
  </li>
  <li>
    تُنظَّم ملفات المشروع هرميًا ودلاليًا؛ وتُخزَّن البيانات الخام، والبيانات المعالجة، والشفرة البرمجية، والمخرجات في مجلدات منفصلة.
    (<span dir="ltr">CC1.2</span>)
  </li>
  <li>
    إنشاء بيانات وصفية مناسبة لجميع مجموعات البيانات، بما في ذلك—على سبيل المثال لا الحصر—
    تاريخ الإنشاء، والمصادر الأولية للبيانات، وقيم الملء أو النطاقات الصالحة، والوحدات.
    (<span dir="ltr">CC1.9</span>)
  </li>
  <li>
    فهم المصفوفات متعددة الأبعاد واستخدامها لتمثيل مجموعات بيانات منظَّمة بحسب المكان والزمان ومتغيّرات متعددة.
    (<span dir="ltr">CC2.3</span>)
  </li>
  <li>
    الإلمام بأنواع مجموعات البيانات المهيكلة المستخدمة في التطبيقات العلمية، بما في ذلك البيانات المكانية (الراستر والمتجهة)
    والبيانات الهرمية (مثل <span dir="ltr">HDF5</span> و<span dir="ltr">netCDF4</span>)؛
    وكيفية قراءتها وإنشاء ملفات بيانات ذاتية التوثيق.
    (<span dir="ltr">CC2.8</span>)
  </li>
  <li>
    اختيار مقاييس ألوان خطيّة إدراكيًا ومناسبة لضعف تمييز الألوان،
    وفهم علاقة المقاييس البصرية بأنواع البيانات الكمية والنوعية المختلفة.
    (<span dir="ltr">CC3.10</span>)
  </li>
  <li>
    توثيق سير العمل الحاسوبي باستخدام تعليقات داخلية ووثائق خارجية
    (مثل ملف <span dir="ltr">README</span> أو توثيق واجهات البرمجة).
    (<span dir="ltr">CC4.3</span>)
  </li>
</ul>

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
مجموعات بيانات المناخ المستخدمة
</h2>

<ul style="direction: rtl; unicode-bidi: plaintext; text-align: right; list-style-position: inside;">
  <li>
    درجات حرارة الهواء اليومية من
    <a dir="ltr" href="https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/">
      مجموعة إعادة التحليل <span dir="ltr">MERRA-2</span> التابعة لمكتب النمذجة والاستيعاب العالمي في ناسا
    </a>.
  </li>
  <li>
    مجاميع الهطول اليومية من
    <a dir="ltr" href="https://disc.gsfc.nasa.gov/datasets/GPM_3IMERGDF_06/summary">
      <span dir="ltr">NASA IMERG-Final</span>
    </a>.
  </li>
  <li>
    بيانات التبخر–النتح، والإشعاع، ورطوبة التربة من
    <a dir="ltr" href="https://disc.gsfc.nasa.gov/datasets/NLDAS_NOAH0125_M_2.0/summary?keywords=NLDAS">
      نظام استيعاب بيانات اليابسة لأمريكا الشمالية (<span dir="ltr">NLDAS</span>) — إعادة التحليل
    </a>.
  </li>
  <li>
    درجة حرارة الهواء والضغط والرطوبة من
    <a dir="ltr" href="https://disc.gsfc.nasa.gov/datasets/NLDAS_FORA0125_M_2.0/summary?keywords=NLDAS">
      بيانات الإمداد (<span dir="ltr">forcing</span>) التابعة لـ <span dir="ltr">NLDAS</span>
    </a>.
  </li>
  <li>
    رطوبة التربة من
    <a dir="ltr" href="https://nsidc.org/data/spl3smp/versions/8">
      مهمة ناسا لرطوبة التربة النشطة/السلبية (<span dir="ltr">SMAP</span>)
    </a>.
  </li>
</ul>

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
شكر وتقدير
</h2>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
تم تمكين هذا المنهج بفضل منحة من برنامج ناسا
<span dir="ltr">Transition to Open Science (TOPS)</span>
للتدريب
(<span dir="ltr">80NSSC23K0864</span>)،
وهو جزء من
<a dir="ltr" href="https://nasa.github.io/Transform-to-Open-Science/">
برنامج <span dir="ltr">TOPS</span> التابع لناسا
</a>.
</p>

</div>

