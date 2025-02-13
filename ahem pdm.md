#notes

*nonton video nya sambil baca yg bagian [[#*ok skrg actually belajar*|disini]], cepetin speed aja klo lambat.*
-  [use case diagram](https://youtu.be/4emxjxonNRI?si=mm9SGbrsaQwW_Ucd&t=85) 
- [class diagram](https://youtu.be/6XrL5jXmTwM?si=Xs9Rr48NhkM_2Efu)
- [state diagram](https://www.youtube.com/watch?v=qICdYjJA-Ps) heres a more[ ribet version](https://www.youtube.com/watch?v=iaX11vYFhZ4)
- [activity diagram](https://youtu.be/Wf_xlagfHmg?si=t9Q_gTYqlGKwVSwk&t=75)
- [sequence diagram](https://youtu.be/pCK6prSq8aw?si=ZYj5V9RdhjANJP4H&t=65)
- ato [himti](https://youtu.be/iZYGGiHflig?feature=shared) if u have trust issues and have the time
## **1. What Are We Doing?**

We are **designing a system** by creating **UML (Unified Modeling Language) diagrams** that visually represent different aspects of the system. The goal is to clarify **how the system works**, how users interact with it, and how different components communicate.

---
## **2. What Are the Steps in System Design?**
### **Step 1: Understanding Requirements** 
*tbh idk why this one matters, gd tutorial yg ngjarin niqqaer, ntr di bwh jg gw ga jelasin KRN GW GTW APA2 ANGJGGGGGGGGGGGGG*
- Identify **Functional Requirements** (what the system must do).
- Identify **Non-Functional Requirements** (how well the system must perform).
### **Step 2: High-Level Overview (Use Case Diagram)**
- Shows **who (actors)** interacts with the system and **what actions** they can perform.
- Helps identify all necessary **features and interactions** before diving into details.
### **Step 3: System Structure (Class Diagram)**
- Defines **the objects (classes)** in the system and their **relationships**.
- Represents **data and operations** that the system must handle.
### **Step 4: Behavior & States**
- **State Diagram**: Shows how objects change **state** over time.
- **Activity Diagrams**: Describe **step-by-step workflows** for key actions like product requests and payments.
### **Step 5: Interaction (Sequence Diagrams)**
- Shows **how different parts communicate** in a **step-by-step interaction**.
- Helps in understanding system **logic and data flow**.
---
##  **TLDR:**

1. **Tentuin dia functional or no** :
	![[Pasted image 20250117030621.png]]
1. **Use Case Diagram** :
	![[Pasted image 20250117030646.png]]
2. **Class Diagram** :
	![[Pasted image 20250117030721.png]]
3. **State and Activity Diagrams** :
	![[Pasted image 20250117030742.png]]
4. **Sequence Diagrams**:
	![[Pasted image 20250117030758.png]]
---

# **ok skrg actually belajar**
---
### **STEP 1: Use case diagram:**
![[Pasted image 20250117033504.png]]
*note: ini gambar ter simplify sama gw, yg di coret biru gausah di anggep*
5. **Buat kotak,** ini jd wadah utk "program" kita dn tulis namany di dlm kotak di plg atas
6. Diluar kotak, **buat stickman di kiri kotak (ini namany actor)** basically user app kita. 
	- kasi nama. namany g hrs user, bisa customer, buyer, anything. (tp yg general)
	- *technically, actor ada primary sama secondary:*
	- *primary: sebagian besar use case terjadi krn dia*
	- *secondary: ya kebalikanny. (ga wajib ada)*
7. **Buat oval** (use cases): step by step app ny jalan.
	- cth m-bca: login, cek saldo, tentuin jmlh transfer, bayar transfer. (**semua diawali kata kerja y nanti**)
8. **Buat garis** (relationships) dari user ke oval yg dia akan jalanin. garis lurus no panah.
	- *ada garis2 lain, (bisa aja gakepake) which are:*
	- *- - -> panah garis putus2: **include** (oval 1 akan selesai klo oval syarat sdh terpenuhi)*
	- *- - -> panah garis putus2: **extend** (oval 2 kemungkinan terjadi tp ga selalu, habis oval 1)*
---
### **STEP 2: Class Diagram:**
![[Pasted image 20250117042528.png]]
9. Buat tabel 1 kolom 3 baris. paling atas tulisanny classnya
	1. contoh: user, binatang, rumah, basically anything bro idk
10. Baris kedua, attributes (kea identifier) baris ke 1.
	1. Cth utk kelas user: nama, umur, tinggi, email, dst.
11. Cara nulis baris kedua:
	1. Atribut pake huruf kecil semua (nama, umur, dst) trs titik 2 and tipe data
	2. nama: string
	3. umur: int
12. Baris tiga: methods:
	1. Kelas ini bisa diapain aja/ bisa ngapain aja. gampangny, program lu perlu ngapain buat ngedata kelas ini?
	2. gantiNama(), getUmur(), dst
13. Visibility: Agak ga penting, kl ga peduli -> semua kecuali nama class, depannya pake tanda `+`
	1. `+` utk atribut/metode itu dibuat public: alias bisa di akses semua kelas
	2. `-` private: cuma kelas itu yg bs pake
	3. `#` protected: ya terbatas, g smua bs pake
	4. `~` package/default: bs dipake semua kelas yg sepaket (gw g ngerti ini mksdny ap tp ok)
14. Relationships: perpanah/garisan
	1. Abstraction: panah dr node baru ke node awal. 
		1. Artinya node baru ini subclass ny class td. Semua metode & atribut dr class awal ikutan ke subclass.
	2. Association: Garis (no panah) dr class ke class. 
		1. misal kelas user-ayamGoreng. (anggep lah ini digarisin y). di garisnya u tulis "makan". Artinya class user makan ayamGoreng. tp si ayamGoreng pny ituanny sendiri kek class biasa. y gt
	3. Aggregation: Garis trs 1 diamond kopong di ujung nya.
		1. Dr class 1 ke class 2 artinya class 1 bisa aja bagian dr class 2, tapi bisa juga engga.
	4. Composition: Garis trs 1 diamond solid di ujungnya.
		1. Dr class 1 ke class 2 artinya class 1 gabisa exist tanpa class 2. misal toilet gbs exist klo gada ruanganny 🤷‍♀️
	5. Multiplicity: taro di garisny composisit class itu cm bs ad brp. idk man tulis aj di semua garis 1 gt.
---

### **STEP 3: State Diagram:**
![[Pasted image 20250117044618.png]]
*ini contoh tercocok sm dosen gw, ignore bulet yg kopong sm bulet ber X. disitu kurang panahny hrsnya ada tulisan dan hrsnya yg kotak pertama di dua2nya itu jg slh IDK BRO INI ANEH BGT MATAKULIAHNYA GADA YG BENER ANJGGGGGGGGGGGGGGGGGGGGGGGGGGG*
15. Buat bulet solid: starting state.
16. Buat rounded square: Ini adalah state (ceritanya status dia skrg kek mana gt)
	1. Misal, state ny `tercatat`
17. Dari starting state, buat panah ke state barunya. Tulis keterangan, apa yg bikin dia sampe ke state itu
	1. Misal, di panah tulisanny `getUsername` ->`[tercatat]` jadi habis getUsername, statusny tercatat. state HARUS kata sifat. Tercatat, terlempar, terklarifikasi, dst. gaboleh "apakah blablabla". Tulisan di panah jg hrs "kata kerja". 
18. Uh, that's basically it tbh.
19. Oh, state diagram itu ada banyak. Ada sebanyak class :)  *ini ajaran dosen gw, bs aj ga bener*
	1. Misal u ada class user, product, belanja. Berarti buat 3 state diagram.
		1. State utk user: `start --getNama, pilihKepentingan--> [tercatat]` 
20. KALO DI GOOGLE DAN VIDEO, hrsnya ada end stateny: bulet solid yg dilingkarin.
	1. tp idk anything dosen gw sampah gw buat kek gt malah disalahin
--- 

### **STEP 4: Activity Diagram:**
![[Pasted image 20250117045601.png]]
*mirip flowchart: rounded square/oval=activity, persegi panjang=class/object, diamond=true or false,*
21. Buat tabel yg misahin siapa yg melakukan proses itu. di contoh b28=org, system=ya sistem
22. Buat bulet solid(start) dgn panah mengarah ke rounded square/oval (nanti akan jd activity state nya) di tempat siapa yg bakal ngestart programny
23.  Tulis di oval itu programny ngapain dst
24. Klo udh selesai, kasih bulet solid yg luarnya dilingkarin lg.
25. udh lol
---

### **STEP 5: Sequence Diagram**
![[Pasted image 20250117055804.png]]
*sambil nonton video y nontonny*
26. Gambar stickman di kiri(?) idk beda2 di video di suruh gt
27. Now, buat kotak2 yg isinya semua objek/class yg hrs berinteraksi sm user selama program berjalan
28. Buatnya berurutan, kiri ke kanan, berdasarkan apa yg dilakuin pertama sm user
29. Buat lifelines: Garis putus2 lurus ke bawah dari kotak2 objek td
	1. lifeline ini ceritany sbg penanda, berapa lama waktu yg sdh lewat, atas itu terbaru, makin ke bawah, makin tua (lama).
30. Buat panah dgn step utk ke objek selanjutnya. Setiap ada panah baru, turun dikit (krn lifeline)
	1. Panahnya nempel dr garis lifeline objek pertama ke objek selanjutnya
	2. Di panah, tulis keterangan actionnya apa
	3. Misal, user --masukin kartu--> ATM
	4. Utk panah selanjutnya, turun dikit!
31. Return lines (panah putus2): basically garis "muter balik" yang ke return
	1. kok di video, yg server ke atm putus2, tapi yang atm ke user engga? karna dia udh "ngereturn" dn skrg dia lagi jalan kaya biasa aja. simpelnya, ***dia cuma putus2 kalo dia garis yg muter balik.***
32. Alternative frame: uhhhhhh nonton lah video nya cuk menit 4.49
	1. buat kotak kek di video gt lah, yg atas jika (kondisi) true, yg bawah else
33. Buat activation boxes: kotakin garis lifeline yang "aktif"
	1. Y gt ad di video