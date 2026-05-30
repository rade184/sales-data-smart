مشروع تدريبي متكامل: خط أنابيب بيانات ونموذج لباور بي آي (Sales Performance Pipeline & Dashboard)
نظرة عامة (Overview):
هذا مشروع تدريبي تطبيقـي مصمم لإثبات القدرة على جلب البيانات الخام غير المهيكلة، معالجتها، بناء نموذج بيانات متكامل، وعرضها في لوحة بيانات تفاعلية في باور بي آي. يعتمد المشروع على بيانات مبيعات تم محاكاتها، ويغطي دورة حياة البيانات بالكامل من البداية وحتى العرض (End-to-End).

خطوات المعالجة والنمذجة (Data Ingestion & Modeling Pipeline):

جلب البيانات الخام (Data Ingestion): تم جلب البيانات الخام الخاصة بالمبيعات والعملاء والمنتجات من مصادرها.

تنظيف وإعداد البيانات (ETL): تم تنفيذ عمليات تنظيف البيانات التالية: معالجة القيم المفقودة، تنسيق التواريخ، التعامل مع البيانات غير المتسقة، وضمان سلامة البيانات قبل البدء في التحليل.

هندسة الميزات (Feature Engineering): تم إضافة أعمدة جديدة لإثراء البيانات وجعلها أكثر اكتمالاً، مثل:

عمدة تاريخية (Date Dimension columns): إنشاء أعمدة "SaleMonthName", "SaleYear", "SaleSeason" لتسهيل التحليل الزمني.

أعمدة مخصصة (Custom Columns): مثل "OrderQuantityBin" أو "CustomerRegion" لزيادة عمق التحليل.

نمذجة البيانات (Data Modeling via Power Pivot): هذه هي الخطوة الأهم. تم إنشاء نموذج بيانات كامل باستخدام Power Pivot:

جداول الأبعاد (Dimension Tables): تم إنشاء جداول أبعاد للعملاء والمنتجات والمتاجر.

جدول الحقائق (Fact Table): تم ربط جداول الأبعاد بجدول الحقائق (Sales).

Star Schema: تم بناء نموذج "Star Schema" لضمان الأداء والدقة. (انظر صورة العلاقات المرفقة).

المقاييس الأساسية (DAX Measures): تم تطوير عدد من المقاييس المخصصة باستخدام لغة DAX لحساب مؤشرات الأداء الرئيسية بدقة، مثل:

Total Sales = SUMX(Sales, Sales[Quantity] * Sales[Unit Price])

Distinct Customers = DISTINCTCOUNT(Sales[CustomerID])

Average Order Value = [Total Sales] / COUNT(Sales[OrderID])

Sales MoM% = ...

العرض البصري (Power BI Dashboard): تم استيراد نموذج البيانات الجاهز وعرضه في لوحة بيانات تفاعلية (image_0.png) لعرض النتائج.

الداشبورد والنتائج البصرية (Final Dashboard):

<img width="1160" height="656" alt="Screenshot 2026-05-26 115733" src="https://github.com/user-attachments/assets/3670c277-8d04-436e-aadd-3fdfb457f5b7" />

مؤشرات الأداء الرئيسية (KPIs): المبيعات الإجمالية، الكمية الإجمالية، العملاء المميزون، ومتوسط قيمة الطلب.

التحليل الزمني (Monthly Sales): مخطط خطي لتتبع المبيعات شهرياً، يظهر قمة في شهر مارس.

الأداء الإقليمي (Sales by Region): مخطط شريطي يظهر أن منطقة الشرق (East) هي الأعلى مبيعاً.

أفضل المنتجات (Top 7 Products): مخطط شريطي يظهر أفضل 7 منتجات.

أفضل العملاء (Top 7 Customers): خريطة شجرية لأعلى 7 عملاء.

حسب الفئة (Sales by Category): مخطط شريطي لأعلى الفئات مبيعاً (الأدوات المكتبية - Office).

حسب المتجر (Sales by StoreID): مخطط دائري يظهر حصة كل متجر.

<img width="1160" height="656" alt="Screenshot 2026-05-26 115733" src="https://github.com/user-attachments/assets/f8849caa-e4aa-44bc-a318-a243c315dcd3" />

المهارات الأساسية المطبقة:

Data Preparation (ETL): جلب البيانات، التنظيف، والتهيئة.

Feature Engineering: هندسة الميزات وزيادة شمولية البيانات.

Data Modeling: بناء نموذج بيانات (Star Schema) باستخدام Power Pivot.

Advanced DAX: كتابة مقاييس مخصصة وحسابات متقدمة.

Visual Storytelling: تصميم لوحة بيانات تفاعلية في Power BI.
