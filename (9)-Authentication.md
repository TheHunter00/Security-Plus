## 1. What is Authentication?

 - هي عملية التحقق من هوية المستخدم أو النظام الذي يحاول الوصول إلى مورد معين. الهدف منها هو التأكد من أن الشخص أو النظام الذي يطلب الوصول هو فعلاً من يدعي أنه هو، وذلك لضمان الأمان وحماية المعلومات.

## 2. Access Control System (ACS)

-  هو مجموعة من القواعد والسياسات التي تحدد من يمكنه الوصول إلى موارد معينة داخل النظام.
- **وظائف ACS:**
  - **تحديد الصلاحيات (Permission Management):** تحديد ما يمكن للمستخدمين أو المجموعات القيام به.
  - **تنفيذ السياسات (Policy Enforcement):** ضمان حماية البيانات والموارد من خلال السياسات الأمنية المعتمدة.

## 3. Objects and Subjects

- **Subject :**

هو الكائن أو الشخص الذي يطلب الوصول.
- **Object :**

هو المورد الذي يريد الموضوع الوصول إليه، مثل الملفات أو قواعد البيانات أو الخدمات.

## 4. Identity and Access Management (IAM)

- هو إطار عمل شامل لإدارة وتوفير الوصول للموارد بناءً على هوية المستخدم.
- **وظائف IAM:**
  - **التسجيل وتسجيل الدخول (Registration and Login):** إدارة كيفية تسجيل المستخدمين والتحقق من هويتهم.
  - **إدارة الأدوار والصلاحيات (Role and Permission Management):** تحديد الأذونات بناءً على أدوار المستخدمين.
  - **مراقبة الوصول (Access Monitoring):** تتبع الأنشطة للتأكد من استخدام الموارد بشكل مناسب.

## 5. Comparison Between ACS and IAM

- **ACS:**
  
 يركز أساساً على كيفية التحكم في الوصول للموارد المحددة.
- **IAM:**

 يشمل إدارة شاملة للهويات، بما في ذلك التسجيل، الأدوار، ومراقبة الوصول بناءً على سياسات شاملة.

## 6. Types of Authentication

1. **Something You Know:**
 - **تعريف:** Information يعرفها المستخدم فقط.
   - **أمثلة:** كلمات المرور (Passwords)، الأرقام السرية (PINs).
   - **ميزات:** سهل الاستخدام لكن يمكن أن يكون عرضة للاختراق إذا كانت كلمات المرور ضعيفة.

2. **Something You Have:**
 - **تعريف:** Physical item يمتلكه المستخدم ويستخدمه للتحقق.
   - **أمثلة:** بطاقات الهوية الذكية (Smart Cards)، التوكنات الأمنية (Security Tokens).
   - **ميزات:** يضيف طبقة أمان إضافية لكن يمكن فقدانه أو سرقته.

3. **Something You Do/Are:**
 - **شيء تفعله (Something You Do):** Activity يتطلب إجراء معين.
     - **أمثلة:** التوقيع الرقمي (Digital Signatures).
   - **شيء تكونه (Something You Are):** Biological characteristics تُستخدم للتعرف.
     - **أمثلة:** بصمة الأصبع (Fingerprint)، التعرف على الوجه (Facial Recognition).
   - **ميزات:** صعب التزوير أو التقليد لكن قد تكون هناك مشاكل في الدقة أو سهولة الاستخدام.

## 7. Authentication Design

عند تصميم نظام المصادقة، يجب مراعاة النقاط التالية:

- **الأمان (Security):** التأكد من أن عملية المصادقة قوية ضد محاولات الاختراق.
- **سهولة الاستخدام (Usability):** يجب أن تكون عملية المصادقة سهلة لتفادي التعقيد الذي قد يؤدي إلى تجاهل الأمان.
- **التوافق (Compatibility):** التأكد من أن النظام متوافق مع التطبيقات والخدمات المستخدمة.

## 8. Multi-Factor Authentication (MFA) and Its Types

- **MFA (Multi-Factor Authentication):**

استخدام عدة عوامل للتحقق من الهوية، مما يعزز الأمان.

  - **2FA (Two-Factor Authentication):**

 يستخدم عاملين فقط للتحقق.
    
 **مثال:** كلمة مرور + رمز يتم إرساله على الهاتف.

  - **3FA (Three-Factor Authentication):**

 يستخدم ثلاثة عوامل للتحقق.
 **مثال:** كلمة مرور + توكن أمان + بصمة أصبع.

---
