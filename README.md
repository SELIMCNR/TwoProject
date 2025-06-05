### **README - İki Aktivite Arasında Intent ile Veri Aktarımı**  -tr

#### **Proje Tanıtımı**  
Bu Android projesi, **iki aktivite arasındaki iletişimi** `Intent` kullanarak nasıl sağlanacağını göstermektedir. Kullanıcı, `MainActivity` ekranında bir `EditText` alanına adını girer ve butona basarak `YeniAktivite` ekranına geçer. Girilen isim ikinci aktiviteye iletilir ve burada bir `TextView` üzerinde gösterilir.  

---

### **Kullanılan Teknolojiler**  
- **Kotlin** (Android uygulama geliştirme)  
- **ViewBinding** (Daha temiz ve güvenli UI yönetimi)  
- **Intent** (Aktiviteler arası veri transferi)  
- **ConstraintLayout** (Esnek ve uyumlu arayüz tasarımı)  

---

### **Proje Yapısı**  
#### **📌 MainActivity.kt**  
- `ViewBinding` ile arayüz elemanlarını yönetir.  
- `sonrakiSayfa(view:View)` fonksiyonu ile `Intent` kullanarak veriyi `YeniAktivite` ekranına gönderir.  
- `Intent.putExtra("isim", gelenYazi)` ile kullanıcıdan alınan veriyi aktarır.  

#### **📌 YeniAktivite.kt**  
- Gönderilen veriyi `intent.getStringExtra("isim")` ile alır.  
- Gelen metni `TextView2` üzerine yerleştirerek ekranda gösterir.  

#### **📌 activity_main.xml**  
- Kullanıcının adını yazacağı **`EditText`** alanı bulunur.  
- **`Button`**, veriyi alıp ikinci aktiviteye göndermek için kullanılır.  
- **`TextView`** eklense de `MainActivity` içinde kullanılmamaktadır.  

#### **📌 activity_yeni_aktivite.xml**  
- Kullanıcıdan gelen ismi ekranda göstermek için **`TextView2`** içerir.  

---

### **Nasıl Çalışıyor?**  
1️⃣ Kullanıcı `EditText` alanına ismini girer.  
2️⃣ **"Sonraki Sayfa"** butonuna bastığında `sonrakiSayfa()` fonksiyonu çağrılır.  
3️⃣ Girilen isim `Intent` ile ikinci aktiviteye aktarılır.  
4️⃣ `YeniAktivite` gelen veriyi alır ve ekranda gösterir.  

---

### **Kurulum & Kullanım**  
1️⃣ Projeyi **Android Studio** ile açın.  
2️⃣ **Emülatör** veya **gerçek cihaz** üzerinden çalıştırın.  
3️⃣ Adınızı girin ve butona basarak ikinci aktiviteye geçiş yapın.  

---

### **README - Transferring Data Between Two Activities with Intent** -eng

#### **Project Introduction**
This Android project demonstrates how to provide **communication** between two activities using `Intent`. The user enters his/her name in an `EditText` field on the `MainActivity` screen and moves to the `NewActivity` screen by pressing the button. The entered name is passed to the second activity and displayed on a `TextView`.

---

### **Technologies Used**
- **Kotlin** (Android application development)
- **ViewBinding** (Cleaner and safer UI management)
- **Intent** (Data transfer between activities)
- **ConstraintLayout** (Flexible and compatible interface design)

---

### **Project Structure**
#### **📌 MainActivity.kt**
- Manages interface elements with `ViewBinding`.

- Sends data to the `NewActivity` screen using `Intent` with the `nextPage(view:View)` function.

- Transfers data received from the user with `Intent.putExtra("name", incomingText)`.

#### **📌 YeniAktivite.kt**
- Receives the sent data with `intent.getStringExtra("name")`.
- Displays the incoming text on the screen by placing it on `TextView2`.

#### **📌 activity_main.xml**
- There is a **`EditText`** field where the user will write their name.
- **`Button`** is used to receive the data and send it to the second activity.
- Although **`TextView`** is added, it is not used in `MainActivity`.

#### **📌 activity_yeni_aktivite.xml**
- Contains **`TextView2`** to display the name sent by the user on the screen.

---

### **How ​​Does It Work?**
1️⃣ The user enters their name in the `EditText` field.
2️⃣ When the **"Next Page"** button is pressed, the `nextPage()` function is called.
3️⃣ The entered name is transferred to the second activity with `Intent`.
4️⃣ `NewActivity` receives the incoming data and displays it on the screen.

---

### **Installation & Usage**
1️⃣ Open the project with **Android Studio**.
2️⃣ Run it on **Emulator** or **real device**.
3️⃣ Enter your name and press the button to switch to the second activity.

---

