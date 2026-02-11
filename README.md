<div dir="rtl" style="direction: rtl; unicode-bidi: isolate; text-align: right;">

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
<a dir="ltr" href="https://zenodo.org/doi/10.5281/zenodo.11204778">
<img src="https://zenodo.org/badge/678572794.svg" alt="DOI" />
</a>
</p>

<h1 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
الوحدة 1: بيانات المناخ المفتوحة
</h1>

<blockquote style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
كيف تُستخدم أقمار ناسا الصناعية، والبيانات الحقلية، والنماذج لتشخيص نظام مناخ الأرض والتنبؤ به؟
وكيف يُقاس التباين المناخي ويُنمذج؟
</blockquote>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
تركّز الوحدة الأولى من
<a dir="ltr" href="https://openclimatescience.github.io/curriculum">منهج علوم المناخ المفتوحة</a>
على تعريف المتعلّمين بمنصة
<span dir="ltr">NASA Earthdata Search</span>
وبالتنوّع الواسع من مجموعات بيانات المناخ التي توفّرها ناسا.
<strong>وبنهاية هذه الوحدة، يُفترض أن تكون قادرًا على:</strong>
</p>

<ul style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
  <li>
    فهم كيفية توليد بيانات المناخ من مجموعات بيانات إعادة التحليل،
    ونماذج الدوران العامة،
    ونماذج نظام الأرض،
    وكيف تختلف هذه النماذج عن بعضها.
  </li>
  <li>
    معرفة أماكن الحصول على المتغيّرات المناخية المختلفة
    (مثل الهطول ودرجة الحرارة)
    بالمقاييس المكانية والزمانية المناسبة.
  </li>
  <li>
    إظهار استخدام متغيّرات مناخية متعددة من مجموعات بيانات مناخية مختلفة.
  </li>
</ul>

<h2 style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
المحتويات
</h2>

<ol style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/01_Sources_of_Climate_Data.ipynb">
      مصادر بيانات المناخ
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/02_Intro_to_NASA_Earthdata_Search.ipynb">
      مقدمة إلى منصة NASA Earthdata Search وبيانات إعادة التحليل
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/03_Reading_MERRA2_Gridded_Climate_Data.ipynb">
      قراءة بيانات المناخ الشبكية MERRA-2
    </a>
  </li>
  <li>
    <a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/notebooks/04_Accessing_MERRA2_Data_in_the_Cloud.ipynb">
      الوصول إلى بيانات MERRA-2 على السحابة
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
<a dir="ltr" href="https://github.com/OpenClimateScience/M1-Open-Climate-Data/blob/main/HOW_TO_INSTALL.md">
اطّلع على دليل التثبيت هنا.
</a>
</p>

<p style="direction: rtl; unicode-bidi: plaintext; text-align: right;">
يمكنك تشغيل دفاتر
<span dir="ltr">Jupyter</span>
في هذا المستودع باستخدام
<a dir="ltr" href="https://docs.github.com/en/codespaces/overview">Github Codespaces</a>
أو كـ
<a dir="ltr" href="https://code.visualstudio.com/docs/devcontainers/containers">حاوية تطوير VSCode</a>.
وبعد تشغيل الحاوية، شغّل Jupyter Notebook عبر:
</p>

<div dir="ltr" style="unicode-bidi: isolate; text-align: left;">
```sh
# أنشئ كلمة مرورك الخاصة عند الطلب
jupyter server password

# ثم شغّل Jupyter Notebook؛ وأدخل كلمة المرور عند الطلب
jupyter notebook
