# Network Fundamentals

## 1. Routing and Switching Protocols

### Routing Protocols

- **RIP (Routing Information Protocol):**
  - **شرح:** بروتوكول للتوجيه يستخدم لتبادل معلومات التوجيه بين أجهزة التوجيه (routers). يقوم بتحديد أفضل طريق لنقل البيانات بناءً على عدد القفزات (hops) للوصول إلى الوجهة.
  - **مثال:** في شبكة تحتوي على عدة أجهزة توجيه، RIP يقوم بتحديث جداول التوجيه في كل جهاز توجيه لتحديد أقصر طريق بناءً على عدد القفزات إلى الوجهة.

- **OSPF (Open Shortest Path First):**
  - **شرح:** بروتوكول يستخدم في الشبكات الكبيرة لتحديد أفضل مسار بناءً على الرسم البياني للشبكة، ويأخذ في اعتباره تكلفة الروابط بين أجهزة التوجيه.
  - **مثال:** في شبكة مكتب كبيرة، OSPF يحدد أفضل طريق لنقل البيانات بين المكاتب المختلفة بناءً على تكلفة الروابط بين أجهزة التوجيه.

- **BGP (Border Gateway Protocol):**
  - **شرح:** البروتوكول الأساسي لتبادل معلومات التوجيه بين الشبكات الكبيرة مثل الإنترنت. يتبادل معلومات حول المسارات الممكنة بين مزودي الخدمة.
  - **مثال:** مزود خدمة الإنترنت يستخدم BGP لتبادل معلومات التوجيه مع مزودي خدمات آخرين، مما يتيح توجيه البيانات عبر الإنترنت بين الشبكات.

### Switching Protocols

- **STP (Spanning Tree Protocol):**
  - **شرح:** بروتوكول يمنع الحلقات (loops) في الشبكة المحلية من خلال إلغاء المسارات المتكررة، مما يضمن توجيه البيانات بشكل صحيح دون تكرار غير ضروري.
  - **مثال:** إذا كانت لديك شبكة LAN تحتوي على عدة مفاتيح (switches) متصلة ببعضها، STP يتأكد من عدم حدوث حلقات بيانات عبر الشبكة.

- **VTP (VLAN Trunking Protocol):**
  - **شرح:** بروتوكول يُستخدم لنقل معلومات VLAN بين مفاتيح الشبكة المختلفة، مما يسهل إدارة VLANs عبر عدة مفاتيح.
  - **مثال:** إذا كان لديك عدة مفاتيح في شبكة LAN، VTP ينسق معلومات VLAN بين المفاتيح لتسهيل إدارتها.

## 2. Layer 2 Forwarding

- **شرح:** عملية توجيه البيانات على مستوى الطبقة 2 من نموذج OSI، حيث يتم استخدام عنوان MAC لتوجيه البيانات إلى الجهاز الصحيح ضمن الشبكة المحلية (LAN).
  - **مثال:** إذا كان جهاز كمبيوتر A يريد إرسال بيانات إلى جهاز كمبيوتر B في نفس الشبكة، يستخدم السويتش عنوان MAC لجهاز الكمبيوتر B لتوجيه البيانات مباشرة إليه.

## 3. MAC Address

- **شرح:** عنوان فريد يُعطى لكل جهاز على الشبكة المحلية لتحديده وتمييزه عن باقي الأجهزة.
  - **مثال:** عنوان MAC لجهاز كمبيوتر قد يكون "00:1A:2B:3C:4D:5E"، ويُستخدم للتعرف على الجهاز ضمن الشبكة.

## 4. IP and IPv4 and IPv6

- **IP Address:**
  - **شرح:** عنوان يُستخدم لتحديد مواقع الأجهزة على الشبكة وتوجيه البيانات بينها.
  - **مثال:** عنوان IP لجهاز كمبيوتر قد يكون "192.168.1.1" في شبكة منزلية.

- **IPv4 (Internet Protocol version 4):**
  - **شرح:** إصدار قديم من عنوان IP يتكون من 32 بت ويوفر حوالي 4.3 مليار عنوان.
  - **مثال:** عنوان IPv4 مثل "192.168.0.1" يستخدم في الشبكات المحلية مثل المنزل أو المكتب.

- **IPv6 (Internet Protocol version 6):**
  - **شرح:** إصدار حديث من عنوان IP يتكون من 128 بت ويوفر عددًا ضخمًا جدًا من العناوين.
  - **مثال:** عنوان IPv6 مثل "2001:0db8:85a3:0000:0000:8a2e:0370:7334" يستخدم في الشبكات الكبيرة التي تحتاج إلى العديد من العناوين.

## 5. NIC and WIC

- **NIC (Network Interface Card):**
  - **شرح:** بطاقة تُركب في جهاز الكمبيوتر لتوفير الاتصال بالشبكة، سواء عبر كابل إيثرنت أو اتصال لاسلكي.
  - **مثال:** بطاقة NIC في جهاز كمبيوتر مكتبي تمكنه من الاتصال بشبكة LAN عبر كابل إيثرنت.

- **WIC (WAN Interface Card):**
  - **شرح:** بطاقة تُستخدم في أجهزة التوجيه لتوفير الاتصال بشبكات WAN مثل الإنترنت.
  - **مثال:** بطاقة WIC في جهاز توجيه تتيح للشركة الاتصال بالإنترنت أو بشبكات أخرى عبر مزود الخدمة.

## 6. DHCP (Dynamic Host Configuration Protocol)

- **شرح:** بروتوكول يُستخدم لتعيين عناوين IP تلقائيًا للأجهزة عند الاتصال بالشبكة، مما يسهل إدارة العناوين.
  - **مثال:** عند توصيل جهاز كمبيوتر جديد بالشبكة، يقوم DHCP بتعيين عنوان IP مثل "192.168.1.101" للجهاز تلقائيًا.

## 7. ARP (Address Resolution Protocol)

- **شرح:** بروتوكول يُستخدم لتحويل عنوان IP إلى عنوان MAC داخل الشبكة المحلية، مما يساعد في توجيه البيانات بشكل صحيح.
  - **مثال:** إذا كان جهاز كمبيوتر A يريد إرسال بيانات إلى جهاز كمبيوتر B، يستخدم ARP لتحديد عنوان MAC لجهاز الكمبيوتر B بناءً على عنوان IP الخاص به.

## 8. Broadcast

- **شرح:** إرسال البيانات إلى جميع الأجهزة في الشبكة المحلية، حيث يتم تلقي الرسالة من كل جهاز متصل بالشبكة.
  - **مثال:** إذا أرسل جهاز كمبيوتر رسالة عبر البث، سيستقبل كل جهاز في شبكة LAN تلك الرسالة.

## 9. Unicast

- **شرح:** إرسال البيانات من جهاز واحد إلى جهاز معين فقط، بدلاً من إرسالها إلى جميع الأجهزة في الشبكة.
  - **مثال:** إذا كان جهاز كمبيوتر A يرسل ملفاً إلى جهاز طابعة محدد، يتم استخدام Unicast لتوجيه البيانات مباشرة إلى الطابعة.

## 10. Source MAC and Destination MAC

- **Source MAC:**
  - **شرح:** عنوان MAC للجهاز الذي يرسل البيانات.
    - **مثال:** إذا كان جهاز كمبيوتر A يرسل بيانات إلى جهاز كمبيوتر B، عنوان MAC لجهاز الكمبيوتر A هو عنوان Source MAC.

- **Destination MAC:**
  - **شرح:** عنوان MAC للجهاز الذي يستقبل البيانات.
    - **مثال:** إذا كان جهاز كمبيوتر A يرسل بيانات إلى جهاز كمبيوتر B، عنوان MAC لجهاز الكمبيوتر B هو عنوان Destination MAC.

## 11. ARP Spoofing

- **شرح:** هجوم يقوم فيه المهاجم بتزوير رسائل ARP لتوجيه البيانات إلى جهاز غير مصرح به، مما يمكنه من سرقة المعلومات أو الإضرار بالشبكة.
  - **مثال:** إذا قام مهاجم بتزوير رسائل ARP في الشبكة، يمكنه توجيه البيانات الحساسة إلى جهازه بدلاً من الجهاز الصحيح، مما يتيح له الوصول غير المصرح به للمعلومات.

## 12. Network Topology and Zone

- **Network Topology:**
  - **شرح:** تصميم الشبكة الذي يحدد كيفية ترتيب وتوصيل الأجهزة ببعضها، وكيفية تدفق البيانات عبر الشبكة.
    - **مثال:** في شبكة نجمية، جميع الأجهزة متصلة بمفاتيح مركزية، مما يساعد في تحسين الأداء وتسهيل الإدارة.

- **Network Zone:**
  - **شرح:** تقسيم الشبكة إلى مناطق مختلفة لتسهيل إدارة الأمان والبيانات.
    - **مثال:** تقسيم الشبكة إلى DMZ لاستضافة خدمات عامة مثل مواقع الويب، ومنطقة داخلية تحتوي على بيانات حساسة.

## 13. DMZ (Demilitarized Zone)

- **شرح:** منطقة في الشبكة تقع بين الشبكة الداخلية والإنترنت، تُستخدم لاستضافة خدمات مثل مواقع الويب التي تحتاج إلى الوصول من الخارج مع حماية الشبكة الداخلية.
  - **مثال:** خادم الويب الخاص بالشركة يوضع في DMZ لتمكين الوصول من الإنترنت مع الحفاظ على أمان الشبكة الداخلية.

## 14. Main Zones

- **LAN (Local Area Network):**
  - **شرح:** شبكة تربط الأجهزة ضمن نطاق جغرافي صغير، مثل المنزل أو المكتب.
    - **مثال:** شبكة المكتب التي تربط أجهزة الكمبيوتر والطابعات داخل نفس المبنى.

- **WAN (Wide Area Network):**
  - **شرح:** شبكة تربط بين مواقع جغرافية بعيدة، مثل فروع مختلفة لشركة أو اتصال بالإنترنت.
    - **مثال:** الشبكة التي تربط مكاتب الشركة في مدن مختلفة عبر الإنترنت.

## 15. Trusted and Untrusted

- **Trusted Network:**
  - **شرح:** شبكة تعتبر آمنة ويُسمح لها بالوصول إلى الموارد الحساسة دون قيود كبيرة.
    - **مثال:** الشبكة الداخلية للشركة التي تحتوي على بيانات حساسة وتخضع لسياسات أمان صارمة.

- **Untrusted Network:**
  - **شرح:** شبكة تُعتبر غير آمنة وتحتاج إلى حماية إضافية عند الوصول إليها.
    - **مثال:** الإنترنت الذي يتم الوصول إليه من خلال شبكة DMZ ويحتاج إلى حماية إضافية لحماية الشبكة الداخلية.

## 16. NAT (Network Address Translation)

- **شرح:** تقنية تُستخدم لترجمة العناوين الخاصة بالشبكة المحلية إلى عنوان IP عام يسمح للأجهزة الداخلية بالاتصال بالإنترنت.
  - **مثال:** في شبكة منزلية، NAT يقوم بترجمة عنوان IP الخاص بجهاز الكمبيوتر (مثل 192.168.1.5) إلى عنوان IP عام (مثل 203.0.113.1) لتمكين الوصول إلى الإنترنت.

## 17. VPN (Virtual Private Network)

- **شرح:** تقنية تُستخدم لإنشاء اتصال آمن بين جهازين أو أكثر عبر شبكة غير موثوقة مثل الإنترنت، مما يحمي البيانات من التجسس.
  - **مثال:** عندما يتصل موظف من المنزل بشبكة الشركة عبر VPN، يتم تشفير البيانات التي يتم إرسالها بين الجهاز والشبكة الداخلية للشركة لضمان الأمان.

## 18. IDS/IPS (Intrusion Detection System / Intrusion Prevention System)

- **IDS (Intrusion Detection System):**
  - **شرح:** نظام يراقب الشبكة أو النظام للكشف عن الأنشطة غير المشروعة أو الهجمات.
    - **مثال:** IDS يمكن أن يكتشف محاولات هجوم عبر الشبكة، مثل محاولة اختراق غير مصرح بها.

- **IPS (Intrusion Prevention System):**
  - **شرح:** نظام يشمل قدرات IDS مع ميزة منع الهجمات أو الأنشطة غير المصرح بها.
    - **مثال:** IPS يمكن أن يمنع محاولات الهجوم تلقائيًا بناءً على قواعد محددة، مثل منع الوصول إلى شبكة معينة من مصدر ضار.

## 19. QoS (Quality of Service)

- **شرح:** تقنية تُستخدم لضمان توفير عرض نطاق ترددي كافٍ للتطبيقات أو الخدمات الهامة، مثل مكالمات الفيديو أو الألعاب، لتقليل تأخير البيانات وتحسين الأداء.
  - **مثال:** في شبكة مكتب، يمكن تكوين QoS لضمان أن مكالمات الفيديو تحصل على أولوية أعلى في عرض النطاق الترددي مقارنةً بتصفح الويب العادي.

## 20. VLAN (Virtual Local Area Network)

- **شرح:** VLAN هو تقسيم منطقي لشبكة LAN إلى عدة شبكات افتراضية، مما يساعد في تحسين الأمان وكفاءة الشبكة.
  - **مثال:** في شركة كبيرة، يمكن إنشاء VLANs مختلفة لقسم المحاسبة، قسم المبيعات، وقسم تكنولوجيا المعلومات بحيث يكون لكل قسم شبكة خاصة به، مما يحسن الأمان والموارد.

## 21. Port Forwarding

- **شرح:** تقنية تُستخدم لتوجيه البيانات من منفذ معين على جهاز توجيه إلى جهاز محدد داخل الشبكة المحلية.
  - **مثال:** إذا كنت تستضيف خادم ويب في منزلك، يمكنك إعداد إعادة توجيه المنافذ لتوجيه طلبات HTTP على المنفذ 80 من جهاز التوجيه إلى عنوان IP الخاص بالخادم.

## 22. SNMP (Simple Network Management Protocol)

- **شرح:** بروتوكول يُستخدم لمراقبة وإدارة الأجهزة على الشبكة، مثل أجهزة التوجيه والمفاتيح والخوادم.
  - **مثال:** يمكن استخدام SNMP لجمع معلومات حول استخدام عرض النطاق الترددي لجهاز توجيه أو مراقبة حالة الخوادم.

## 23. Network Segmentation

- **شرح:** تقسيم الشبكة هو عملية تقسيم الشبكة الكبيرة إلى أجزاء أصغر لتقليل الازدحام وزيادة الأمان.
  - **مثال:** يمكن تقسيم الشبكة إلى أقسام مختلفة مثل الشبكة الإدارية، الشبكة العامة، وشبكة الزوار لتحسين الأداء والأمان.

## 24. Firewall Rules

- **شرح:** قواعد تُستخدم لتحديد ما إذا كان يجب السماح أو منع مرور البيانات عبر الجدار الناري بناءً على معايير محددة مثل عنوان IP، رقم المنفذ، أو نوع البروتوكول.
  - **مثال:** يمكنك إعداد قاعدة لجدار ناري للسماح فقط للاتصالات الواردة على المنفذ 80 (HTTP) من شبكة معينة، بينما تمنع جميع الاتصالات الأخرى.

## 25. Proxy Server

- **شرح:** خادم يُستخدم كوسيط بين المستخدمين والإنترنت لتقديم خدمات مثل تحسين الأداء، توفير الأمان، والتحكم في الوصول.
  - **مثال:** في مكتب، يمكن استخدام خادم وكيل لتحسين سرعة الوصول إلى المواقع من خلال التخزين المؤقت للبيانات، وكذلك لتصفية المحتوى ومنع الوصول إلى مواقع غير مرغوب فيها.

