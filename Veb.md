# Final İmtahan Hovuzu — Cavablar
**Fənn:** UI/UX Veb Dizayn | **Mövzu sayı:** 15 | **Sual sayı:** 60

---

## 🛠️ Praktiki Tapşırıq (bütün mövzularda təkrarlanan sual)

> *"Sizdən e-commerce mövzusunda 2 səhifəlik veb sayt interfeysi hazırlamağınız gözlənilir..."*

Bu tapşırıq imtahan hovuzunda 14 dəfə təkrarlanır, ona görə tam həll planı **bir dəfə**, aşağıda ətraflı verilir. Hər bir mövzu bölməsində bu sualın qarşısında yalnız bu bölməyə istinad qoyulub.

### Həll planı

**1. Hazırlıq mərhələsi**
- E-commerce sahəsi seçilir (məs. geyim, elektronika, kosmetika mağazası).
- İstifadəçi yol xəritəsi (user flow) qurulur: İstifadəçi ana səhifəyə daxil olur → kateqoriyaya baxır → məhsul səhifəsinə keçir → "Səbətə əlavə et" düyməsini sıxır.
- Sadə wireframe eskizi kağız üzərində və ya Figma-da aparılır.

**2. Figma-da struktur qurulması**
- Frame ölçüsü: Desktop (1440×1024 px və ya 1920×1080 px).
- Grid sistemi: 12 sütunlu grid, sütun arası boşluq (gutter) 24px, kənar boşluq (margin) 80–120px.
- Rəng palitrası: 1 əsas rəng, 1 əlavə (accent) rəng, neytral boz çalarlar (mətn, fon üçün).
- Tipoqrafiya: başlıqlar üçün bold sans-serif (məs. Inter, Poppins), gövdə mətni üçün adi çəki, ölçü iyerarxiyası (H1 32–40px, H2 24px, body 14–16px).

**3. Ana səhifə (Home page)**
- Naviqasiya paneli (logo, menyu, axtarış, səbət ikonu).
- Hero bölməsi (banner, CTA düyməsi).
- Məhsul kateqoriyaları və ya seçilmiş məhsullar grid şəklində kartlarla göstərilir.
- Footer (əlaqə, sosial şəbəkə linkləri).

**4. Məhsul detalı səhifəsi**
- Məhsul şəkli (böyük), adı, qiyməti, qısa təsviri.
- "Səbətə əlavə et" və "İndi al" düymələri.
- Ölçü/rəng seçimi kimi əlavə UI elementləri (dropdown, radio button).
- Oxşar məhsullar bölməsi səhifənin aşağısında.

**5. Komponentləşdirmə**
- Düymə, kart, naviqasiya paneli, input sahəsi ayrıca **Component** kimi yaradılır ki, hər yerdə təkrar istifadə oluna bilsin (Repetition prinsipi).
- Auto Layout istifadə olunaraq elementlərin ölçüsü responsiv saxlanılır.

**6. Prototipləşdirmə**
- Frame-lər arasında keçid: Ana səhifədəki məhsul kartına klik → Məhsul detalı səhifəsinə keçid.
- Ən azı bir neçə interaction əlavə olunur: düymə üzərinə **Hover** effekti (rəng dəyişməsi), klikdə **Smart Animate** keçidi.
- Prototip rejimində "Flow" işə salınaraq test edilir.

**7. Təqdimat**
- Dizaynın hansı prinsiplərə (vizual iyerarxiya, proximity, repetition, alignment) əsaslandığı qısa izah olunur.
- Rəng və şrift seçiminin niyə belə olduğu, istifadəçi rahatlığının necə təmin olunduğu bildirilir.

**Qiymətləndirmə meyarları:** struktur ardıcıllığı, vizual iyerarxiya, komponent istifadəsi, prototipin işlək olması, ümumi vahid üslub.

---

## Mövzu 1 — Dizayn prinsipləri

**1. Veb səhifənin struktur elementləri hansılardır və onların funksiyaları nələrdir?**
Veb səhifənin əsas struktur elementləri: **header** (loqo, naviqasiya, axtarış), **hero/banner bölməsi** (əsas mesaj və CTA), **əsas məzmun (content) sahəsi**, **sidebar** (əlavə naviqasiya və ya filtr), və **footer** (əlaqə, hüquqi məlumat, sosial linklər). Header istifadəçiyə oriyentasiya və naviqasiya imkanı verir, content sahəsi əsas informasiyanı ötürür, footer isə əlavə, lakin vacib resurslara çıxış təmin edir. Bu elementlərin düzgün təşkili istifadəçinin səhifədə rahat hərəkət etməsini və məqsədinə tez çatmasını təmin edir.

**2. İstifadəçi yol xəritəsi (user flow) nədir və veb dizayn prosesində necə tətbiq olunur?**
User flow istifadəçinin müəyyən məqsədə (məs. alış-veriş etmək) çatmaq üçün izlədiyi addımların ardıcıl sxemidir. Dizayn prosesində o, səhifələr arası məntiqi keçidləri planlaşdırmaq, lazımsız addımları aradan qaldırmaq və istifadəçi təcrübəsini sadələşdirmək üçün istifadə olunur. Adətən giriş nöqtəsindən (məs. ana səhifə) başlayaraq son hədəfə (məs. sifarişin təsdiqi) qədər bütün qərar nöqtələri diaqram şəklində göstərilir, bu da prototip qurarkən əsas baza rolunu oynayır.

**3. Vizual iyerarxiya nədir və dizaynda hansı məqsədlə istifadə olunur?**
Vizual iyerarxiya elementlərin ölçü, rəng, kontrast və yerləşmə baxımından elə təşkil olunmasıdır ki, istifadəçinin diqqəti ən vacib məlumata ilk növbədə yönəlsin. Məqsəd informasiyanın əhəmiyyət dərəcəsinə uyğun şəkildə qavranılmasını təmin etməkdir — məsələn, böyük və qalın başlıq əvvəlcə görünür, sonra alt başlıq, daha sonra adi mətn. Bu, istifadəçinin səhifəni daha sürətli "oxumasına" və əsas hərəkətə (CTA) yönəlməsinə kömək edir.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 2 — Dizayn prinsipləri

**1. Tipoqrafik iyerarxiya ilə ümumi vizual iyerarxiya arasında hansı fərq mövcuddur?**
Tipoqrafik iyerarxiya yalnız mətn elementlərinin (başlıq, alt başlıq, gövdə mətni) ölçü, çəki və üslub fərqləri ilə əhəmiyyət sırasının göstərilməsidir. Ümumi vizual iyerarxiya isə daha geniş anlayışdır və rəng, məkan, kontrast, ölçü kimi bütün qrafik elementləri əhatə edir. Yəni tipoqrafik iyerarxiya vizual iyerarxiyanın yalnız bir hissəsidir — mətnə aiddir, digəri isə bütöv səhifə kompozisiyasına.

**2. Proximity (yaxınlıq) prinsipi elementlər arasında əlaqəni necə göstərir?**
Proximity prinsipinə görə bir-birinə yaxın yerləşdirilmiş elementlər istifadəçi tərəfindən məntiqi əlaqəli kimi qəbul edilir, uzaq yerləşdirilənlər isə ayrı qruplar kimi görünür. Məsələn, bir məhsul kartında şəkil, ad və qiymət bir-birinə yaxın yerləşdirilərsə, istifadəçi onları avtomatik olaraq vahid məlumat bloku kimi qavrayır. Bu prinsip qruplaşdırma vasitəsilə interfeysin oxunaqlılığını artırır.

**3. Repetition (təkrar) prinsipi dizaynda vahid üslub yaratmaq üçün necə istifadə olunur?**
Repetition prinsipi eyni vizual elementlərin (rəng, şrift, düymə forması, ikon üslubu) bütün dizayn boyunca təkrarlanmasıdır. Bu, istifadəçiyə tanışlıq hissi verir və interfeysin bütöv, peşəkar görünməsini təmin edir. Məsələn, bütün düymələrin eyni künc radiusu və rəngi olması istifadəçiyə "bu da kliklənə bilən elementdir" siqnalını ardıcıl şəkildə ötürür.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 3 — Xətalar və istifadəçi nəzarəti

**1. İstifadəçi interfeysində xətaların qarşısını almaq üçün hansı üsullardan istifadə olunur?**
Xətaların qarşısını almaq üçün: aydın etiketləmə, məcburi sahələrin işarələnməsi, real-vaxt validasiya (input yazıldıqca yoxlanılması), məhdudlaşdırıcı UI elementləri (dropdown, slider — açıq mətn sahəsi əvəzinə), təsdiqləmə dialoqları (silmə kimi geri dönməz əməliyyatlar üçün) və default dəyərlərin düzgün seçilməsi istifadə olunur. Bu üsullar istifadəçinin səhv məlumat daxil etmə ehtimalını minimuma endirir.

**2. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**3. Form doldurularkən istifadəçiyə nəzarət və rahatlıq təmin etmək üçün hansı UI elementlərindən istifadə olunur?**
Form dizaynında istifadəçiyə nəzarət hissi vermək üçün: aydın label-lar, placeholder mətnlər, irəliləyiş göstəricisi (progress bar — çoxmərhələli formalarda), real-vaxt validasiya işarələri (yaşıl ✓ / qırmızı ✗), avtomatik doldurma təklifləri, geri qayıtmaq imkanı və yığcam, məntiqi sıra ilə düzülmüş sahələr istifadə olunur. Bu elementlər istifadəçinin prosesi başa düşməsini və idarə edə bilməsini asanlaşdırır.

**4. İstifadəçinin səhv əməliyyat etməsinin qarşısını almaq üçün interfeys necə dizayn olunmalıdır?**
İnterfeys təbii qərar prosesinə uyğun, aydın və minimal qeyri-müəyyənliklə dizayn olunmalıdır. Vacib və ya geri dönməz əməliyyatlar (silmə, ödəniş) üçün əlavə təsdiqləmə tələb olunmalı, səhv kliklərin qarşısını almaq üçün düymələr arasında kifayət qədər məsafə saxlanılmalı, sistem həmişə istifadəçiyə cari vəziyyət haqqında geri bildirim (feedback) verməlidir. Konsistent naviqasiya və proqnozlaşdırıla bilən davranış da xəta ehtimalını azaldır.

---

## Mövzu 4 — İstifadəçi interfeysinin proqram arxitekturası

**1. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**2. Single Page Application (SPA) nədir və adi veb saytdan fərqi nədir?**
SPA — bütün tətbiq tək HTML səhifəsi üzərində işləyən, səhifə tam yenilənmədən (reload) JavaScript vasitəsilə dinamik məzmun yükləyən veb tətbiqdir (məs. Gmail, Facebook). Adi (çoxsəhifəli) veb saytda hər keçiddə server yeni HTML səhifəsi qaytarır və brauzer tam yenilənir. SPA daha sürətli, daha "tətbiq kimi" təcrübə verir, lakin ilkin yüklənmə daha ağır ola bilər və SEO baxımından əlavə tənzimləmə tələb edir.

**3. MVC arxitekturasında Model, View və Controller nə iş görür?**
**Model** — məlumatları və biznes məntiqini idarə edir (verilənlər bazası ilə iş). **View** — istifadəçiyə göstərilən vizual təqdimatdır (interfeys). **Controller** — istifadəçi hərəkətlərini qəbul edir, Model-ə müraciət edir və nəticəni View-da əks etdirir. Bu üçlük ayrılığı kodun strukturlaşdırılmasını, dəstəklənməsini və komanda daxilində paralel işləməni asanlaşdırır.

**4. İstifadəçi interfeysində komponent anlayışı nədir və necə istifadə olunur?**
Komponent — təkrar istifadə oluna bilən, müstəqil UI vahididir (düymə, kart, naviqasiya paneli və s.). O, bir dəfə yaradılır və lazım olan hər yerdə istifadə olunur, dəyişiklik isə yalnız "ana" komponentdə edilərək bütün nüsxələrə avtomatik tətbiq olunur. Bu, dizayn sisteminin ardıcıllığını qoruyur, inkişaf prosesini sürətləndirir və baxımı asanlaşdırır.

---

## Mövzu 5 — Sistem menyuları və naviqasiya sxemləri

**1. "Wireframe" və "Mockup" anlayışlarını müqayisə edin və dizayn prosesində onların rolunu izah edin.**
Wireframe — səhifənin struktur skeletidir, rəng və detallar olmadan, yalnız elementlərin yerləşməsini göstərir; məqsəd erkən mərhələdə layoutu və funksionallığı təsdiqləməkdir. Mockup isə rəng, tipoqrafiya, şəkillər daxil olmaqla, son məhsula çox yaxın statik vizual təqdimatdır. Wireframe ideyanı sürətlə sınamaq üçün, mockup isə müştəri ilə son görünüşü razılaşdırmaq üçün istifadə olunur — ikisi dizayn prosesinin ardıcıl mərhələləridir.

**2. "Hamburger menu" nədir və hansı hallarda istifadə olunur?**
Hamburger menu — üç üfüqi xətdən ibarət ikona ilə təmsil olunan, kliklənəndə gizli naviqasiya siyahısını açan UI elementidir. Əsasən ekran sahəsi məhdud olan mobil interfeyslərdə, çox sayda menyu bəndini kompakt saxlamaq üçün istifadə olunur. Desktop dizaynında isə yer kifayət qədər olduğundan adətən tam görünən naviqasiya üstünlük təşkil edir.

**3. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**4. Breadcrumb (çörək qırıntısı) naviqasiyası nədir və istifadəçiyə nə kimi fayda verir?**
Breadcrumb — istifadəçinin sayt iyerarxiyasında hazırkı yerini göstərən, ardıcıl linklərdən ibarət naviqasiya zolağıdır (məs. Ana səhifə > Geyim > Kişi köynəkləri). O, istifadəçiyə hazırkı mövqeyini anlamağa, bir kliklə əvvəlki səviyyəyə qayıtmağa kömək edir və dərin struktura malik saytlarda itkinlik hissini azaldır.

---

## Mövzu 6 — Veb miqyaslı tədqiqat metodları

**1. Veb dizaynda istifadəçi davranışını analiz etmək üçün hansı tədqiqat metodları mövcuddur?**
Əsas metodlara aiddir: **usability testing** (real istifadəçilərlə tapşırıq icrası izlənilir), **A/B testing** (iki versiya müqayisə edilir), **heatmap/click tracking** (klik və skroll davranışı vizuallaşdırılır), **sorğular və müsahibələr**, **analitika alətləri** (Google Analytics — gediş tezliyi, vaxt göstəriciləri) və **card sorting** (məlumat arxitekturasını test etmək üçün). Bu metodların kombinasiyası həm kəmiyyət, həm keyfiyyət məlumatı verir.

**2. Veb dizaynda "usability testing" nədir və əsas məqsədi nədir?**
Usability testing — real istifadəçilərin müəyyən tapşırıqları interfeysdə icra etməsinin müşahidə olunması prosesidir. Əsas məqsəd dizaynın nə dərəcədə intuitiv, effektiv və istifadəçi üçün rahat olduğunu müəyyən etmək, çətinlik yaradan nöqtələri (pain points) aşkarlayıb düzəltməkdir. Bu, real istifadədən əvvəl problemləri tapmaq imkanı verir və yekun məhsulun keyfiyyətini artırır.

**3. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**4. A/B testing nədir və dizayn qərarlarını yoxlamaqda necə istifadə olunur?**
A/B testing — eyni səhifənin iki fərqli versiyasının (A və B) istifadəçilərin müxtəlif qruplarına eyni vaxtda göstərilərək hansının daha yaxşı nəticə (konversiya, klik dərəcəsi) verdiyinin statistik müqayisəsidir. Dizaynerlər bununla, məsələn, düymə rəngi, başlıq mətni və ya layout variantları arasında subyektiv fikir əvəzinə real istifadəçi datasına əsaslanan qərar verirlər.

---

## Mövzu 7 — Prototipləşdirmə

**1. Figma-da prototipləşdirmə nədir və nə üçün istifadə olunur?**
Figma-da prototipləşdirmə statik dizayn frame-lərini bir-biri ilə interaktiv keçidlərlə (link) birləşdirərək, kliklənə bilən, real tətbiq təcrübəsini simulyasiya edən nümunə yaratmaqdır. Bu, dizaynın istifadəçi tərəfindən sınanmasını, komandanın və müştərinin fikrini development başlamazdan əvvəl almasını mümkün edir, beləliklə vaxt və resurs itkisinin qarşısı alınır.

**2. Frame-lər arasında keçid (interaction) necə qurulur?**
Figma-da Prototype rejimində bir elementin (məs. düymə) sağ kənarındakı dairədən tutub hədəf frame-ə sürükləməklə bağlantı yaradılır. Sonra "trigger" (On Click, On Hover və s.), "action" (Navigate to, Open overlay, Swap) və "animation" (Instant, Smart Animate, Dissolve) parametrləri seçilərək keçidin davranışı təyin olunur.

**3. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**4. Figma-da "Prototype" bölməsində hansı əsas ayarlar mövcuddur və onlar nə üçün istifadə olunur?**
Əsas ayarlara aiddir: **Trigger** (hərəkəti işə salan hadisə — klik, hover, sürükləmə), **Action** (nə baş verəcəyi — naviqasiya, overlay açılması, geri qayıtma), **Animation** (keçid effekti — Instant, Smart Animate, Slide, Dissolve) və **Device frame** (test edilən qurğu növü). Bu ayarlar dizaynerə real tətbiq davranışına çox yaxın interaktiv təcrübə qurmağa imkan verir.

---

## Mövzu 8 — Qrafik dizayn

**1. Qrafik dizaynda vizual iyerarxiya nədir və istifadəçi diqqətini yönləndirməkdə necə rol oynayır?**
Qrafik dizaynda vizual iyerarxiya ölçü, rəng kontrastı, məkan və forma vasitəsilə baxışın səhifədə müəyyən ardıcıllıqla hərəkət etməsini təmin edir. Diqqəti ilk növbədə ən vacib elementə (məs. başlıq və ya CTA düyməsi) yönəldərək, istifadəçinin informasiyanı sürətli və düzgün ardıcıllıqla qəbul etməsinə kömək edir.

**2. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**3. Kompozisiya anlayışı qrafik dizaynda nəyi ifadə edir və uğurlu kompozisiya üçün hansı amillər vacibdir?**
Kompozisiya — vizual elementlərin (mətn, şəkil, boşluq) bir-biri ilə tarazlı və məqsədəuyğun şəkildə düzülməsidir. Uğurlu kompozisiya üçün balans, kontrast, proporsiya, boş sahə (white space), fokus nöqtəsi və ritm vacibdir. Bu amillərin düzgün tarazlığı dizaynı həm estetik, həm də funksional cəhətdən effektiv edir.

**4. Vizual elementlərin ölçü və yerləşimi (scale və alignment) mesajın qəbuluna necə təsir edir?**
Böyük ölçülü elementlər daha vacib, kiçik elementlər isə ikinci dərəcəli kimi qəbul edilir — bu, diqqəti idarə etməyin əsas vasitəsidir. Alignment (düzülüş) isə elementlər arasında görünməz, lakin hiss olunan əlaqə yaradır; düzgün düzülməmiş elementlər xaotik görünür və etibarlılıq hissini azaldır, məntiqi düzülüş isə peşəkarlıq və oxunaqlılığı artırır.

---

## Mövzu 9 — Verilənlərin vizuallaşdırması

**1. Figma-da verilənlərin vizuallaşdırılması üçün "Auto Layout" istifadə edərək bar chart necə qurulur?**
Hər sütun üçün ayrıca düzbucaqlı (rectangle) yaradılır, onların hündürlüyü göstərmək istənilən qiymətə uyğunlaşdırılır. Bu sütunlar bir "frame" daxilinə yığılır və həmin frame-ə **Auto Layout** (üfüqi istiqamətdə) tətbiq olunur — bu, sütunlar arasında bərabər məsafəni avtomatik saxlayır. Hər sütunun altına label əlavə edilir, dəyər dəyişdikdə Auto Layout strukturu avtomatik yenidən düzür.

**2. Veb dizaynda verilənlərin vizuallaşdırılmasında "label" və "legend" elementlərinin funksiyası nədir?**
**Label** konkret data nöqtəsinin və ya oxun nə ifadə etdiyini göstərir (məs. ay adı, rəqəm dəyəri). **Legend** isə qrafikdə istifadə olunan rəng/simvolların hansı kateqoriyaya uyğun gəldiyini izah edir. Hər ikisi qrafiki izahsız da anlaşılan edir və məlumatın səhv yozulmasının qarşısını alır.

**3. Figma-da grid sistemindən istifadənin əsasları.**
Grid sistemi səhifəni sütun (column), boşluq (gutter) və kənar (margin) əsasında bölərək elementlərin düzgün və ardıcıl yerləşməsini təmin edir. Figma-da Layout Grid funksiyası vasitəsilə (sütun, sətir və ya kvadrat grid növləri) frame üzərinə tətbiq olunur, bu da dizaynerə bütün səhifələrdə vahid uyğunlaşma (alignment) saxlamağa kömək edir.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 10 — Rəng dizaynı və tipoqrafiya

**1. Veb dizaynda rənglərin psixoloji təsiri və düzgün rəng seçiminin əhəmiyyəti nədir?**
Rənglər istifadəçidə müəyyən emosional reaksiyalar yaradır — məsələn, mavi etibar və sakitlik, qırmızı təcililik və enerji, yaşıl isə təbiilik və təhlükəsizlik hissi yaradır. Brendin xarakterinə uyğun rəng seçimi istifadəçi etibarını artırır, CTA düymələri üçün kontrastlı rənglər isə hərəkətə təşviq dərəcəsini yüksəldir. Səhv rəng seçimi isə istifadəçidə yanlış emosional assosiasiyalar yarada bilər.

**2. Rəng nəzəriyyəsi çərçivəsində hue, saturation və lightness (HSL) komponentlərinin qarşılıqlı təsiri vizual qavrayışa necə təsir edir?**
**Hue** rəngin əsas tonunu (qırmızı, mavi və s.), **Saturation** rəngin canlılıq dərəcəsini (boz-aşırı parlaq aralığında), **Lightness** isə rəngin işıqlılıq/qaranlıq səviyyəsini müəyyən edir. Bu üç parametrin balanslı dəyişdirilməsi vahid rəng palitrası (ton ailəsi) yaratmağa, müxtəlif vəziyyətlər (hover, disabled, active) üçün məntiqi variasiyalar qurmağa imkan verir, həddindən artıq saturasiya isə gözü yorur və oxunaqlılığı azaldır.

**3. Serif və sans-serif şriftlərin qavrayış baxımından fərqləri nələrdir və bu fərqlər hansı kontekstlərdə funksional üstünlük yaradır?**
Serif şriftlərin hərflərinin ucunda kiçik "ayaqcıqlar" var, bu da çap mətnlərində gözün sətir boyunca hərəkətini asanlaşdırır və ənənəvi, etibarlı görünüş yaradır. Sans-serif şriftlər isə təmiz, sadə xətlərə malikdir və ekranlarda, xüsusən kiçik ölçülərdə daha aydın oxunur. Ona görə veb interfeyslərdə əsasən sans-serif (UI mətnləri üçün), bəzən serif isə uzun məqalə və ya rəsmi kontekstlərdə üstünlük təşkil edir.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 11 — Əlçatanlıq və universal dizayn

**1. WCAG standartları nədir və niyə UI/UX dizaynda tətbiq olunur?**
WCAG (Web Content Accessibility Guidelines) — veb məzmunun əlil və ya məhdud imkanlı istifadəçilər (görmə, eşitmə, motor məhdudiyyəti olan) üçün əlçatan olmasını təmin edən beynəlxalq standartlar toplusudur. Dizaynda tətbiqi bütün istifadəçilərin bərabər imkanlarla saytdan istifadə edə bilməsini, hüquqi tələblərə uyğunluğu və daha geniş auditoriyaya çatmağı təmin edir.

**2. Alternativ mətn (alt text) nədir və hansı hallarda istifadə olunur?**
Alt text — şəklin məzmununu mətnlə təsvir edən atributdur, ekran oxuyucu proqramları (screen reader) tərəfindən görmə qabiliyyəti olmayan istifadəçilərə oxunur. Şəkil yüklənmədikdə də əvəzedici mətn kimi göstərilir. Bütün informativ şəkillərdə (logo, məhsul şəkli, infoqrafika) istifadə olunmalı, dekorativ şəkillərdə isə boş buraxıla bilər.

**3. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**4. Veb dizaynda əlçatanlıq təmin etmək üçün hansı əsas texniki tələblər tətbiq olunur?**
Əsas tələblərə aiddir: kifayət qədər rəng kontrastı (mətn/fon arasında ən azı 4.5:1), klaviatura ilə tam naviqasiya imkanı, bütün şəkillərə alt text, formalarda aydın label-lar, fokus vəziyyətinin (focus state) vizual olaraq görünməsi, video/audio üçün subtitr və transkript təmin edilməsi. Bu tələblər bütün istifadəçi qruplarının saytdan rahat istifadəsini təmin edir.

---

## Mövzu 12 — Heuristic qiymətləndirmə

**1. Heuristic qiymətləndirmə nədir və əsas məqsədi nədir?**
Heuristic qiymətləndirmə — bir neçə ekspertin interfeysi əvvəlcədən müəyyən edilmiş istifadə qaydaları (heuristikalar, məs. Nielsen-in 10 prinsipi) əsasında nəzərdən keçirərək problemləri aşkar etdiyi qiymətləndirmə metodudur. Əsas məqsəd real istifadəçi testindən əvvəl, az xərclə və sürətlə əsas usability problemlərini tapıb düzəltməkdir.

**2. Heuristic qiymətləndirmə zamanı hansı prinsiplərə əsaslanılır?**
Ən çox istifadə olunan əsas — Jakob Nielsen-in heuristikalarıdır: sistemin vəziyyətinin görünməsi, sistem və real dünya uyğunluğu, istifadəçi nəzarəti və azadlığı, ardıcıllıq və standartlar, xətaların qarşısının alınması, tanınma (yaddan çıxarma əvəzinə), çeviklik, estetik və minimalist dizayn, xəta mesajlarının köməyi, sənədləşmə/yardım.

**3. Heuristic qiymətləndirmənin əsas üstünlükləri və çatışmazlıqları nələrdir?**
**Üstünlükləri:** sürətli, ucuz, real istifadəçi cəlb etmədən erkən mərhələdə tətbiq edilə bilər. **Çatışmazlıqları:** ekspertlərin subyektiv mülahizəsinə əsaslanır, real istifadəçi davranışını tam əks etdirmir, bəzi kontekstual problemləri (real istifadə şəraitində yaranan) aşkar edə bilməz, ona görə adətən usability testing ilə tamamlanmalıdır.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 13 — Animasiya

**1. İnteraktivlik veb dizaynın hansı mərhələlərində və necə tətbiq olunur?**
İnteraktivlik prototipləşdirmə mərhələsində (klikləmə, hover effektləri ilə) və final development mərhələsində (CSS/JS animasiyaları, real funksionallıq) tətbiq olunur. Dizayn prosesində əvvəlcə statik vəziyyətlər (default, hover, active, disabled) müəyyənləşdirilir, sonra onlar arasındakı keçidlər (animasiya, vaxt, easing) planlaşdırılır ki, istifadəçi sistemin reaksiyasını aydın hiss etsin.

**2. Mikrointeraksiyalar (microinteractions) nədir və harada istifadə olunur?**
Mikrointeraksiyalar — kiçik, funksional animasiya və ya geri bildirim elementləridir (məs. "like" düyməsinə klikdə ürəyin animasiyası, yüklənmə zamanı spinner, bildiriş səsi). Onlar istifadəçi hərəkətinin sistem tərəfindən qəbul edildiyini bildirir, interfeysi daha canlı və başa düşülən edir; düymələr, formalar, bildirişlər kimi yerlərdə geniş istifadə olunur.

**3. CSS-də "transition" və "animation" anlayışları arasında hansı fərq var?**
**Transition** bir CSS xassəsinin (rəng, ölçü və s.) bir vəziyyətdən digərinə (məs. hover zamanı) sadə, bir mərhələli keçidini təmin edir və adətən hadisə (event) tələb edir. **Animation** isə `@keyframes` vasitəsilə çoxmərhələli, müstəqil və təkrarlana bilən mürəkkəb hərəkətlər yaratmağa imkan verir, hadisə olmadan da avtomatik işə düşə bilər.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

## Mövzu 14 — İnterfeyslərin qiymətləndirilməsi texnikaları

**1. Saytın funksional strukturunun qurulması mərhələlərini izah edin.**
Əsas mərhələlər: (1) tələblərin analizi və məqsədin müəyyənləşdirilməsi, (2) məlumat arxitekturasının (information architecture) qurulması — səhifələrin və kateqoriyaların iyerarxiyası, (3) sitemap yaradılması, (4) wireframe-lərin hazırlanması, (5) vizual dizayn (mockup), (6) prototipləşdirmə və test, (7) development və yekun yoxlama. Bu ardıcıllıq strukturun məntiqli və istifadəçi yönümlü olmasını təmin edir.

**2. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

**3. Heuristic qiymətləndirmə ilə usability testing arasında əsas fərq nədir?**
Heuristic qiymətləndirmə ekspertlər tərəfindən, qaydalar əsasında, real istifadəçi olmadan aparılır — sürətli, lakin subyektivdir. Usability testing isə real istifadəçilərin konkret tapşırıqları icra etməsi əsasında aparılır və real davranışı, çətinlikləri obyektiv şəkildə üzə çıxarır, lakin daha çox vaxt və resurs tələb edir. İkisi bir-birini tamamlayan metodlardır.

**4. Cognitive walkthrough nədir və hansı məqsədlə istifadə olunur?**
Cognitive walkthrough — ekspertlərin özlərini yeni istifadəçi yerinə qoyaraq, addım-addım müəyyən tapşırığı icra edərkən hər addımda "İstifadəçi bunu görəcəkmi? Düzgün addımı seçəcəkmi? Geri bildirim alacaqmı?" sualları əsasında interfeysi qiymətləndirməsidir. Məqsəd ilk dəfə istifadə edən şəxslər üçün öyrənmə əyrisini (learnability) qiymətləndirməkdir.

---

## Mövzu 15 — Mobil istifadəçi interfeysi

**1. Mobil tətbiqlərdə bottom navigation nədir və niyə istifadə olunur?**
Bottom navigation — ekranın aşağı hissəsində yerləşən, əsas bölmələrə (adətən 3-5) tez keçid təmin edən sabit naviqasiya panelidir. Baş barmaqla əlçatan zona olduğundan, mobil qurğularda bir əllə istifadəni rahatlaşdırır və istifadəçinin tətbiqin əsas funksiyalarına həmişə bir kliklə çata bilməsini təmin edir.

**2. Mobil UI dizaynında responsive və adaptive dizayn arasında hansı fərq var?**
**Responsive dizayn** vahid, çevik layout istifadə edir, elementlər ekran ölçüsünə uyğun olaraq nisbi vahidlərlə (%, fr) avtomatik dəyişir. **Adaptive dizayn** isə əvvəlcədən müəyyən edilmiş bir neçə sabit ekran ölçüsü (breakpoint) üçün ayrıca, fərqli layout versiyaları hazırlayır. Responsive daha çevik, adaptive isə hər ölçü üçün daha dəqiq nəzarət imkanı verir.

**3. Mobil və desktop interfeys dizaynı arasında əsas fərqlər nələrdir?**
Mobil dizaynda ekran sahəsi məhduddur, ona görə naviqasiya sadələşdirilir (hamburger/bottom nav), elementlər barmaqla toxunma üçün böyüdülür (touch target ən azı 44×44px), vertikal scroll üstünlük təşkil edir. Desktop dizaynda isə daha çox sahə, hover effektləri, mürəkkəb çoxsütunlu layoutlar və siçan əsaslı dəqiq klik mümkündür.

**4. Praktiki sual** — bax: yuxarıdakı "Praktiki Tapşırıq" bölməsi.

---

*Sənəd 15 mövzu üzrə 60 final sualını əhatə edir (45 nəzəri sual fərdi cavablandırılıb, 15 praktiki sual isə vahid həll planına istinadla cavablandırılıb).*
