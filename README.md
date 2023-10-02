# Bagian Head
Pertama-tama di bagian head, saya menuliskan link yang akan saya perlukan kedepannya, seperti link dari font awesome untuk ikon dan link dari google font untuk pengambilan font
```css
<!DOCTYPE html>
<html>

<head>
    <title>Club Member Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"/>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Pixelify Sans">
```
# Membuat Style
Ada cukup banyak class yang saya buat untuk project ini, akan saya bedah satu-satu ya

#Class untuk membuat Navigation Bar
```css
<style type="text/css">
        .inline-menu>li {
            display: inline;
            list-style-type: none;
            margin-right: 60px;
        }

        .navbar {
            background-color: #1d1d1d;
            padding: 15px;
            border-radius: 10px;
        }

        .navbar-link {
            color: #fffbf5;
        }
```

#Untuk mengatur main font yang akan dipakai pada website ini 
```css
body {
            max-width: 100rem;
            margin: auto;
            font-family: sans-serif;;
        }
```

#Class untuk font Pixelify yang di ambil dari google font
```css
.pixelify {
            font-family: "Pixelify Sans";
            font-size: 21px;, 
        }
```

#Class untuk mengatur posisi isi konten (Kartu nama yang akan dibuat)
```css
.content {
            margin-left: 35px;
            margin-right: 35px;
        }
```

#Class untuk mengatur posisi dan ukuran gambar pertama
```css
.imgOne-body {
            display: block;
            margin: 0 auto;
            width: 50%;
            border-radius: 15px;
        }
```

#Class untuk membuat frame kartu member
```css
 .card {
            width: 802.5px;
            height: 472.441860465px; 
            position: relative;
            border: 2px solid #000; 
            border-radius: 25px; 
            margin: auto;
            transition: transform 0.3s ease;
        }
```

#Class untuk memasukan gambar ke dalam card, nanti nya akan dimasukkan ke dalam class card
```css
.card-image img {
            max-width: 100%;
            max-height: 100%;
            position: absolute;
            top: 0;
            left: 0;
        }
```

#Class untuk memberikan efek zoom ketika kursor mengarah ke card
```css
.card:hover {
        transform: scale(1.1); /* Buat efek Zoom */
        }
```

#Class untuk mengatur text yang akan ada di dalam card khususnya untuk text profile
```css
.card-text {
        position: absolute;
        top: 10px; 
        left: 350px; 
        color: #1d1d1d; 
         }
```

#Class untuk mengatur text yang akan ada di dalam card khususnya untuk text QR-Code
```css
.qr-text {
        position: absolute;
        top: 330px; 
        left: 130px; 
        color: #1d1d1d; 
        line-height: 0.3; 
         }
```

#Class untuk mengatur text tambahan yang nanti nya terletak di bawah card, text berisi "Get Your Own Membership" dan link jika ingin mendaftar
```css
.membership-menu {
            padding-left: 50px;
        }
```

#Class untuk mengatur text pada h1
```css
.h1 {
            text-align: center;
            color: #1d1d1d;
        }
```

#Class untuk mengatur text pada h3
```css
.h3 {
            text-align: center;
            color: #1d1d1d;
        }
```

#Class untuk membuat efek bounce pada ikon api yang terletak di profile text zodiac, ikon api ini diambil dari link font awesome
```css
 @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateY(0);
        }
        40% {
            transform: translateY(-20px);
        }
        60% {
            transform: translateY(-10px);
        }
    }

        .fire-icon {
        animation: bounce 0.5s ease infinite; 
        }
    </style>
</head>
```

# Bagian Body
Setelah selesai membuat class yang akan kita perlukan, saat nya mengisi konten nya di bagian body html

#Mari kita membuat Navigation Bar nya dulu
```html
<body>
    

    <div class="navbar">
        <ul class="inline-menu">
            <li style="margin-left: -35px;">
                <a class="navbar-link" href="#">Home</a>
            </li>
            <li>
                <a class="navbar-link" href="#">About</a>
            </li>
            <li>
                <a class="navbar-link" href="#">Contact</a>
            </li>
        </ul>
    </div>
```
Disini saya membuat navigation bar dengan class navbar yang sudah dibuat sebelum nya, lalu di dalam class navbar terdapat class inline-menu guna nya agar list tidak memanjang kebawah tapi ke samping, lalu di dalam nya juga terdapat class navbar-link guna nya untuk memberi warna pada garis bawah nya, kurang lebih seperti ini looks nya :

![Screenshot 2023-10-02 150304](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/42bce41c-682e-4d00-94f1-c603cd6d34b6)


#Lalu mulai memasukan isi konten dibawah Navigation Bar dimulai dengan class content
```html
<div class="content">
        <h1 class="h1"> KEIKO STUDIO <i class="far fa-copyright"></i></h1>
        <hr />

        <img class="imgOne-body" src="C:\CCIT UI\SEMESTER 3\MAP & WAP\WAP\CardOne.png" />
```
Disini di dalam class content saya membuat title web nya terlebih dahulu yaitu KEIKO STUDIO dengan ikon copyright yang saya ambil dari font awesome, dibawah nya saya kasih garis horizontal sebagai pemisah dengan konten selanjutnya, yaitu gambar dari logo dari KEIKO STUDIO yang saya design sendiri lewat aplikasi lain. Tampilan nya akan menjadi seperti ini :

![Screenshot 2023-10-02 194632](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/ea9251a4-1f54-4514-924e-b95dc39d39e6)


#Nah sekarang yuk kita bikin kartu member nya, masih di dalam class content
```html
<div class="card">
        <div class="card-image">
            <img src="C:\CCIT UI\SEMESTER 3\MAP & WAP\WAP\CardTwo.png" alt="Foto Latar Belakang" style="border-radius: 25px;">
            <img src="C:\CCIT UI\SEMESTER 3\MAP & WAP\WAP\FotoSaya3.png" alt="Foto Wajah Saya" style="width: 30%; height: auto; left: 47px; right: 47px; top: 20px;">
            <img src="C:\CCIT UI\SEMESTER 3\MAP & WAP\WAP\QR Code.jpg" style="width: 10%; height: auto; left: 47px; right: 47px; top: 310px;">
        </div>
```
Jadi di dalam class content, kita memasukkan class yaitu class card, dan di dalam class card terdapat class card-image. Ini class yang di khususkan untuk membuat card profile member, disini kita akan membentuk frame nya dan memasukkan isi konten untuk card profile, di codingan diatas, kita baru memasukan konten gambar saja, looks nya akan menjadi seperti ini :

![Screenshot 2023-10-03 001132](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/e8cdca70-9eb7-4d14-abaa-ff1b3463df04)


#Oke sekarang card nya sudah terbentuk, kita tinggal menambahkan text di dalam card nya
```html
<div class="card-text">
                <h3><span style="font-family: sans-serif;">N</span><span
                    class="pixelify">A</span><span style="font-family: sans-serif;">ME</span></h3>
                <p>Keiko Joceliandita</p>
                <h3><span style="font-family: sans-serif;">OCC</span><span
                    class="pixelify">U</span><span style="font-family: sans-serif;">PATI</span><span
                    class="pixelify">O</span><span style="font-family: sans-serif;">N</span></h3>
                <p>Social Media Specialist</p>
                <h3><span style="font-family: sans-serif;">H</span><span
                    class="pixelify">O</span><span style="font-family: sans-serif;">BBIES</span></h3>                
                <li>Going To The Gym</li>
                <li>Overthinking</li>
                <li>Watching Grey's Anatomy & Modern Family</li>
                <h3><span style="font-family: sans-serif;">ZODI</span><span
                    class="pixelify">A</span><span style="font-family: sans-serif;">C</span></h3>
                <p>Aries <i class="fas fa-fire fire-icon"></i></p>
                
            </div>
```

Masih di dalam class card, kita memasukkan lagi class card-text ke dalam class card, class card-text ini berisikan khusus untuk text yang akan di masukkan ke dalam card profile bagian biodata. Disini saya sadar membuat list dengan li tanpa menggunakan ul. Alasan nya adalah ketika saya otak atik, jika menggunakan ul maka posisi text khusus bagian list nya akan sedikit bergeser ke arah kanan, sedangkan jika saya hapus ul nya posisi text nya jadi lebih rapih dan sejajar. Saya juga menggunakan span seperti yang sudah bapak ajarkan minggu lalu, agar dalam 1 kalimat bisa memakai font yang berbeda, kurang lebih looks nya akan seperti ini :

![Screenshot 2023-10-03 001823](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/59fd0853-e687-418d-a674-d459ee20812c)

#Finishing card profile nya

Oke card kita sudah terbuat dan terisi, tinggal hal terakhir menambahkan text tambahan untuk informasi di foto QR-Code nya
```html
<div class="qr-text">
                <p style="font-size: smaller;">SCAN THIS!</p>
                <h4>GET TO KNOW ME</h4>
            </div>
            
        </div>
    </div>
```

Masih di dalam class card, saya menambahkan satu class lagi yaitu class qr-text, untuk text tambahan mengenai informasi gambar QR-Code nya yang ada di card profile, sekaligus mengakhiri isi dari class card. Looks nya akan menjadi seperti ini :

![Screenshot 2023-10-03 003008](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/52b0e19f-fcdf-4733-951c-4981334869ba)


#Last Step

Oke card profile kita telah selesai sekarang saya mau menambahkan informasi tambahan di luar dari isi card profile nya, jadi ini text yang berisikan, "GET YOUR OWN MEMBERSHIP NOW" serta list link nya. Tujuan nya supaya seperti web ke anggotaan pada umum nya yang pasti nya ada CTA untuk join membership.
```html
<h3>GET YOUR OWN MEMBERSHIP NOW!</h3>
        <ul class="membership-menu">
            <li>
                <p>
                    <a href="https://web.whatsapp.com/">Whatsapp <i class="fab fa-whatsapp"></i></a>
                </p>
            </li>
            <li>
                <p>
                    <a href="https://mail.google.com/">Email <i class="far fa-envelope"></i></a>
                </p>
            </li>
        </ul>

    </div>
</body>

</html>
```

Code diatas sekaligus mengakhiri codingan yang saya buat, dan code diatas masih masuk ke dalam class content ya. Untuk membuat list saya sudah mengatur nya ke dalam class membership-menu. Saya juga menambahkan link dan ikon di tiap list, seperti link dan ikon whatsapp dan email. Saya mau sedikit jelasin secara garis besar bagian body untuk class nya karena seperti nya kebanyakan class ya, biar gak bingung saya jelasin ulang.

Jadi di bagian body terdapat 9 class :
1. Class navbar -> Berguna untuk membuat navigation bar, di tulis di paling pertama bagian body
2. Class inline-menu -> Terletak di dalam class navbar. Berguna agar list yang ada di navbar tidak memanjang kebawah tapi ke samping, untuk mengatur jarak text di dalam navbar nya juga
3. Class navbar-link -> Terletak di dalam class navbar. Berguna untuk memberi warna garis bawah pada text yang ada di navbar nya
4. Class content -> Bisa dibilang ini adalah main class nya, berisikan semua isi konten website setelah navigation bar, literally semua
5. Class card -> class ini terletak di dalam class content. class ini ditujukan khusus untuk pembuatan card profile, segala isi dari card profile yang akan dimasukkan ada di class ini
6. Class card-image -> Class ini terletak di dalam class card. Class ini guna nya untuk memasukkan semua file foto/gambar yang dibutuhkan / yang ingin dimasukkan ke dalam card profile nya, seperti foto wajah, foto cover card nya, foto logo dari KEIKO STUDIO, dan foto QR-Code
7. Class card-text -> Class ini terletak di dalam class card. Class ini berisikan text tentang profile untuk card yang saya buat
8. Class qr-text -> Class ini terletak di dalam class card. Class ini berisikan text tentang informasi lebih lanjut dari gambar QR-Code yang terdapat pada card profile
9. Class membership-menu -> Class ini terletak di dalam class content. Dia tidak masuk ke dalam class card karena posisi nya berada di luar bagian card profile. Class ini hanya untuk mengatur jarak list saja

Ok itu saja penjelasan singkat dari website yang saya buat, dan overall looks nya akan tampak seperti ini :
![Screenshot 2023-10-03 010139](https://github.com/walkeyzz/Tugas-WAP/assets/146419451/49c0c067-7238-4337-b7e6-bbc6ad0310a1)

Oh iya selain jika kursor mengarah ke card nya akan ada efek zoom. Ikon api nya juga ada animation looping, jd dia bouncing terus ikon nya. Biar gemes hehe.






















