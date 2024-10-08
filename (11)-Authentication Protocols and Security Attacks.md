## Local Network and Remote Authentication

**Local Network Authentication**:
- يشير إلى عملية التحقق من هوية المستخدمين الذين يحاولون الوصول إلى الموارد على نفس الشبكة المحلية.
- بمعنى آخر، المصادقة تتم داخل الشبكة نفسها، مثل شبكة المكتب أو المنزل.

**Remote Authentication**:
- يتعلق بالتحقق من هوية المستخدمين الذين يحاولون الوصول إلى الشبكة أو الموارد من موقع بعيد عبر الإنترنت.
- تتطلب هذه العملية أمانًا أعلى نظرًا لأن البيانات تمر عبر الإنترنت.

## Windows Authentication

**Windows Authentication**:
- **NTLM (NT LAN Manager)**:

هو بروتوكول قديم ولكنه لا يزال مستخدمًا.
  
يعتمد على كلمات السر ويقدم مستويات أمان محدودة.

- **Kerberos**:

هو بروتوكول أحدث وأكثر أمانًا.
يعتمد على استخدام التذاكر لتأكيد الهوية، مما يعزز الأمان بشكل كبير.

## Linux Authentication

**Linux Authentication**:
- **PAM (Pluggable Authentication Modules)**:

هو نظام مرن يسمح باستخدام طرق متعددة للتحقق من الهوية.
مثل بصمات الأصابع أو بطاقات الهوية.

## SSO (Single Sign-On)

**Single Sign-On (SSO)**:
- يتيح لك تسجيل الدخول مرة واحدة فقط للوصول إلى جميع التطبيقات والخدمات التي لديك صلاحية للوصول إليها.
  - يقلل من الحاجة لإدخال اسم المستخدم وكلمة السر لكل خدمة على حدة، مما يوفر الوقت ويعزز الأمان.

## Kerberos Authentication

**Kerberos Authentication**:
- هو بروتوكول مصادقة يعتمد على **تذاكر**.
  - عندما يقوم المستخدم بتسجيل الدخول، يحصل على **TGT (Ticket-Granting Ticket)**، والتي يستخدمها للحصول على تذاكر أخرى للوصول إلى خدمات محددة على الشبكة دون الحاجة لإعادة إدخال بيانات الدخول.

## Active Directory

**Active Directory (AD)**:
- هو نظام من مايكروسوفت لإدارة معلومات المستخدمين والأجهزة على الشبكة.
  - يوفر أدوات لإدارة الأذونات وتطبيق السياسات الأمنية عبر **Group Policies**، والتي تساعد في تنظيم وضبط إعدادات الأمان على الأجهزة المتصلة.

## KDC (Key Distribution Center)

**KDC (Key Distribution Center)**:

هو مكون رئيسي في نظام **Kerberos** يحتوي على قسمين:

    
   - **AS (Authentication Server)**:

يتحقق من هوية المستخدم ويصدر TGT.

   - **TGS (Ticket-Granting Service)**:

يستخدم TGT لإصدار تذاكر للوصول إلى خدمات محددة.

## TGT (Ticket-Granting Ticket)

**TGT (Ticket-Granting Ticket)**:
- هي تذكرة يُعطى للمستخدم بعد عملية تسجيل الدخول الناجحة.
  - تُستخدم للحصول على تذاكر أخرى للوصول إلى خدمات مختلفة على الشبكة.

## PAP, CHAP, and MS-CHAP Authentication

**PAP (Password Authentication Protocol)**:
- هو بروتوكول مصادقة بسيط يستخدم كلمات السر للتحقق من الهوية.
  - لكنه غير آمن لأن كلمة السر تُرسل نصًا.

**CHAP (Challenge-Handshake Authentication Protocol)**:
- هو بروتوكول يوفر أمانًا أكبر من PAP.
  - عن طريق استخدام عملية تحقق دورية تعتمد على بيانات المصادقة بدلاً من إرسال كلمة السر بشكل مباشر.

**MS-CHAP (Microsoft Challenge-Handshake Authentication Protocol)**:
- هو تحسين لـ CHAP.
  - ويستخدم في شبكات مايكروسوفت لتقديم مستوى أمان أعلى.

## Password Attacks

**Password Attacks**:
- **Brute Force Attack**: محاولة تجربة جميع الاحتمالات الممكنة لكسر كلمة السر.
- **Dictionary Attack**: استخدام قائمة بكلمات شائعة لتخمين كلمة السر.
- **Credential Stuffing**: محاولة استخدام كلمات السر التي تم تسريبها في اختراقات سابقة على حسابات مختلفة.
- **Social Engineering**: استخدام الخداع للحصول على معلومات حساسة مثل كلمات السر من المستخدمين.

## MD5 and SHA

**MD5 (Message Digest Algorithm 5)**:
- هو خوارزمية تجزئة قديمة، تحول البيانات إلى قيمة ثابتة الطول.
  - لكن تحتوي على مشكلات أمان مثل التصادمات، مما يجعلها غير موصى بها حاليًا.

**SHA (Secure Hash Algorithm)**:
- هو مجموعة من خوارزميات التجزئة الأحدث والأكثر أمانًا.
  - مثل **SHA-256** و **SHA-3**، والتي توفر أمانًا أفضل من MD5.

## Plaintext/Unencrypted Attacks

**Plaintext/Unencrypted Attacks**:
- تشير إلى الهجمات التي تستهدف البيانات غير المشفرة.
  - مثل هجمات **Man-in-the-Middle**، حيث يمكن للمهاجمين التنصت على البيانات أو تعديلها أثناء انتقالها عبر الشبكة.

## Online Attacks

**Online Attacks**:
- **Session Hijacking**: سرقة جلسة مستخدم للوصول إلى الموارد بدون الحاجة لكلمة سر.
- **Brute Force Attack**: محاولة تجربة جميع الاحتمالات مباشرة على النظام للوصول إلى كلمات السر.

## Have I Been Pwned Website

**Have I Been Pwned**:
- هو موقع يمكنك من التحقق مما إذا كانت معلوماتك الشخصية أو كلمات السر تم تسريبها في اختراقات سابقة.
  - يساعدك في اتخاذ إجراءات لتأمين حساباتك.

## Offline Attack

**Offline Attack**:
- هجمات تُنفذ على بيانات مشفرة تم استخراجها مسبقًا.
  - مثل **Hash Cracking**، حيث يتم محاولة كسر التجزئة للحصول على كلمات السر.

## Dump

**Dump**:
- هو استخراج جميع البيانات من قاعدة بيانات أو نظام.
  - وقد يشمل معلومات حساسة مثل كلمات السر في شكل **Memory Dump**.

## Brute Force and Dictionary Attacks

**Brute Force Attack**:
- محاولة تجربة كل الاحتمالات لكسر كلمات السر.
  - وعادة ما تكون عملية تستغرق وقتًا طويلاً.

**Dictionary Attack**:
- محاولة استخدام قائمة بكلمات شائعة لتخمين كلمات السر.
  - وهي أسرع من **Brute Force**.

## Rainbow Attacks

**Rainbow Table Attack**:
- استخدام جداول مسبقة تحتوي على قيم تجزئة للكلمات السرية لتسريع عملية كسر التشفير.

## Salt

**Salt**:
- هو قيمة إضافية تُضاف لكلمة السر قبل تجزئتها لزيادة الأمان ولجعل الهجمات مثل Rainbow Table أقل فعالية.

**Pepper**:
- قيمة أمان إضافية تُضاف على مستوى عالمي لتقوية الأمان.

## Hybrid Attacks

**Hybrid Attacks**:
- هجمات تجمع بين تقنيات مختلفة.
  - مثل استخدام قاموس كلمات السر مع تعديلات محددة لتكوين كلمات سر أقوى.

**Rainbow Table with Salt**:
- هجمات تستخدم **Rainbow Tables** مع **Salt**.
  - مما يتطلب جداول تجزئة خاصة تحتوي على قيم **Salt**.

