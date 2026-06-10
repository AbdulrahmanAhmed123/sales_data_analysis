# 📊💰 E-Commerce Sales Data Analysis & Insights

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-purple.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange.svg?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Charts-blue.svg?style=for-the-badge)](https://seaborn.pydata.org/)

Welcome to the **E-Commerce Sales Data Analysis** project! This repository showcases an end-to-end data analytics framework designed to explore, clean, and extract high-value business insights from transactional sales data. It translates raw historical rows into actionable intelligence regarding revenue trends, customer behaviors, and product performance.

---

## 🚀 Project Overview (نظرة عامة على المشروع)

الهدف الأساسي من المشروع هو الإجابة على الأسئلة الاستراتيجية التي تهم أي شركة تجارة إلكترونية أو مدير مبيعات (Sales Director):
1. **Revenue Growth Metrics:** تتبع نمو المبيعات والأرباح عبر الفترات الزمنية المختلفة (شهرياً وسنوياً).
2. **Product Performance Analysis:** تحديد المنتجات والفئات (Categories) الأكثر مبيعاً والأكثر ربحية.
3. **Customer Behavior Segmentation:** فهم طبيعة سلوك الشراء لدى العملاء وتحديد أفضل الأسواق جغرافياً.
4. **Data-Driven Decision Making:** تقديم توصيات مبنية على الأرقام لتحسين المخزون وتوجيه الحملات التسويقية.

---

## ⚙️ Data Analytics Pipeline (خطوات سير العمل)

[Raw Transactional Sales CSV] ──> [Data Discovery & Structure Exploration]
│
▼
[Data Cleaning & Feature Engineering]
- Formatting Dates, Handling Nulls, Fixing Outliers
│
▼
[Exploratory Data Analysis (EDA)]
- Aggragations, GroupBy Summaries, Sales Trends
│
▼
[Executive Insights & Data Visualizations]
- Dynamic Matplotlib & Seaborn Corporate Layouts


---

## 🛠️ Phase 1: Data Preprocessing & Cleaning (تجهيز البيانات وتنظيفها)

البيانات الخام دائماً ما تحتوي على عيوب تعيق التحليل الدقيق. باستخدام مكتبات `pandas` و `numpy`، قمنا ببناء تنظيف صارم للداتا:
* **Handling Missing & Duplicate Rows:** رصدنا القيم الفارغة في الأعمدة الأساسية وتم التعامل معها، بالإضافة إلى حذف السجلات المكررة لعدم تضخيم الأرقام.
* **Date-Time Standardisation:** تحويل أعمدة التواريخ من نصوص (Strings) إلى صيغة `datetime` صريحة لتسهيل عملية الـ Time-Series Analysis واشتقاق أعمدة فرعية مثل (الشهر، السنة، اليوم).
* **Data Consistency:** تعديل أنواع البيانات (Data Types) للأعمدة المالية لضمان دقة العمليات الحسابية.
* **Anomaly Elimination:** فحص القيم المتطرفة (Outliers) في الكميات المباعة والأسعار لضمان عدم تشويه المتوسطات الحسابية للمبيعات.

---

## 📈 Phase 2: Exploratory Data Analysis (التحليل الاستكشافي)

هنا قمنا باستجواب البيانات واستخراج الأرقام الإجمالية والمؤشرات الرئيسية (KPIs) باستخدام تجميعات متقدمة `groupby` و `agg`:

### 📊 Strategic Analytical Matrix
الأسئلة الرئيسية التي تمت الإجابة عليها برمجياً وإحصائياً:

| Business Question | Technical Execution | Visual Output |
| :--- | :--- | :--- |
| **ما هو الشهر الأعلى مبيعاً؟** | `groupby('Month')['Sales'].sum()` | Line Chart (اتجاه المبيعات) |
| **ما هي المنتجات الأكثر طلباً؟** | `groupby('Product')['Quantity'].sum()` | Horizontal Bar Chart |
| **أين تتركز القوة الشرائية؟** | `groupby('City')['Sales'].sum()` | Geographic Distribution Bar |
| **ما هو أفضل توقيت للإعلانات؟** | `groupby('Hour')['Sales'].count()` | Peak Hours Peak Curve |

---

## 🎨 Phase 3: Visual Storytelling & Corporate Charts (الرسوم البيانية)

باستخدام مكتبات **Matplotlib** و **Seaborn**، قمنا بتحويل الأرقام الجافة إلى لوحات بصرية مريحة ومفهومة لأي شخص غير تقني:
* **Sales Trend Curve:** رسم خط بياني يوضح مسار المبيعات على مدار العام لتحديد مواسم الذروة (Seasonality) وفترات الركود.
* **Top Performing Products:** رسم بياني شريطي (Bar Chart) يعرض الترتيب التنازلي للمنتجات الأكثر تحقيقاً للإيرادات لتسهيل اتخاذ قرارات إدارة المخزون.
* **Hourly Order Volume:** رسم بياني يوضح تذبذب عدد الطلبات على مدار الـ 24 ساعة، وهو ما يساعد فريق التسويق في تحديد الأوقات الذهبية لإطلاق الحملات الإعلانية المموّلة.

---

## 💡 Executive Business Insights (أبرز النتائج والتوصيات)

* **مواسم الذروة:** أظهر التحليل أن هناك فترات معينة في السنة (مثل نهاية العام) تشهد قفزة جنونية في المبيعات، مما يستدعي تأمين المخزون قبلها بوقت كافٍ.
* **المنتجات الرابحة:** تم تحديد فئات معينة من المنتجات تستحوذ على نصيب الأسد من الأرباح، بينما توجد منتجات أخرى ذات تكلفة عالية وعائد ضعيف يُوصى بتقليل الاعتماد عليها.
* **سلوك المشتري:** وجدنا أن أغلب عمليات الشراء تتركز في ساعات محددة (مثلاً من 11 صباحاً إلى 12 ظهراً، ومن 7 إلى 9 مساءً)، وهي الأوقات الأمثل للتواصل مع العملاء.

---

## 📂 Repository Structure (هيكل ملفات المشروع)

```text
├── Sales_DataAnalysis.ipynb  # الـ Jupyter Notebook الأساسي اللي فيه الكود والتحليل والرسوم
├── Sales_Data.csv           # ملف البيانات الخام للمبيعات (الـ Dataset)
├── README.md                 # التوثيق الشامل والشرح التفصيلي للمشروع (الملف الحالي)
└── requirements.txt          # ملف المكتبات اللازمة لتشغيل المشروع
🚀 How to Run Locally (تشغيل المشروع على جهازك)
اعمل Clone للمشروع عندك:

Bash
git clone [https://github.com/AbdulrahmanAhmed123/sales_data_analysis.git](https://github.com/AbdulrahmanAhmed123/sales_data_analysis.git)
cd sales_data_analysis
طبّق المكتبات اللازمة لتشغيل البيئة:

Bash
pip install pandas numpy matplotlib seaborn jupyter
افتح الـ Jupyter Notebook واستمتع بالتحليل:

Bash
jupyter notebook Sales_DataAnalysis.ipynb



# sales_data_analysis
[salesAnalyst.pptx](https://github.com/user-attachments/files/15931632/salesAnalyst.pptx)


[salesAnalyst.pdf](https://github.com/user-attachments/files/15931631/salesAnalyst.pdf)

![1](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/e2df867d-434e-4a12-8dfa-27b555b0628a)
![3](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/0ec2eb05-416a-418b-a6ff-a74a2d75a542)
![2](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/1234d51b-ee14-46a6-a5d9-089ef0f61290)
![7](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/b7a41980-8ab4-4388-986d-cf195e2e927b)
![6](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/4284b20a-a42a-4d19-8a80-fa85f35a32f4)
![5](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/7bf5f2a4-4e66-4a8b-9368-f621c23de8f1)
![4](https://github.com/AbdulrahmanAhmed123/sales_data_analysis/assets/95978956/2f031949-c79d-4305-96de-6030e32893b8)
