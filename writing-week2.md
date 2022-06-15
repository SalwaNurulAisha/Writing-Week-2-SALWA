# JAVASCRIPT SCOPE
* cara memproses data pada pemograman dalam ruang lingkup tertentu.
* JavaScript Scope terbagi menjadi 2 :

  **1. Global Scope**
   - variabel dideklarasi di luar blocks
   - dapat diakses dimanapun dalam suatu file

        ``` js
        let myName = 'Salwa';
        function greeting() {
            return myName;
        }
        console.log(myName);
        ```

  **2. Global Scope**
   - variabel dideklarasi di dalam blocks
   - hanya bisa diakses di dalam blocks

        ``` js
        function greeting() {
        let myName = 'Nurul';
            return myName;
        }
        console.log(greeting());
        ```

    > Blocks ini tuh maksudnya kode pemograman yang dijalankan di dalam ***curly bracket*** {}


# JAVASCRIPT FUNCTION
* blok kode dalam sebuah grup untuk menyelesaikan 1 task dan kode itu bisa digunakan kembali
* pada function terdapat ***greeting***, itu disebut ***identifier*** atau identitas dari sebuah variabel
* pada function terdapat 2 hal yg diperlukan, yaitu:

  **1. Parameter Function** 
     sebuah inputan data untuk melakukan tugas.

  **2. Argumen Function**
     nilai untuk melakukan pemanggilan functionnya, dimana jumlahnya harus sama dengan parameter
* parameter dan argumen tersebut dimasukan ke dalam tanda kurung () atau bisa disebut dengan **info**
  
    ![javascript function](/assets/images/function.PNG)

* **Default Parameter** : pemberian nilai awal langsung dibagian parameter. 
     > sehingga menjaga function agar tidak error saat dipanggil tanpa argumen.
* **Function Helper** : dapat digunakan untuk menspesifikasikan satu buah fungsi /
     > function yang udah dibuat bisa digunakan pada function lain


# JAVASCRIPT OBJECT
* tipe data variabel yang dapat mengkombinasikan tipe data lainnya (number, boolean, string, dll)
* object ini menyimpan properti dan method pada sebuah variabel
* kode cara membuat object
    > let namaObject = { key: 'value'}
     - key atau properties merupakan data lengkap dari sebuah object.
     - value ini isi dari sebuah key.
* Untuk mengakses key / property terdapat 2 cara :
  
  **1. Dot notation**
     ```js
      let person ={
      nama: 'Salwa',
      umur: 19,
      hoby: 'menggambar',
      }
      console.log(person.hoby);
     ```

   - memanggil value dengan menggunakan titik (dot).
   - tidak bisa digunakan untuk menjalankan value yang menggunakan spasi.
    
  **2. Bracket notation**
     ```js
      let person ={
      nama: 'Salwa',
      umur: 19,
      hoby: 'menggambar',
      'makanan kesukaan' : 'tahu'
      }
      console.log(person['makanan kesukaan']);
     ```

   - memanggil value dengan menggunakan square bracket [].
   - dapat digunakan untuk menjalankan value yang menggunakan spasi.

* **Const in Object** : update nilai object (menambahkan nilai), namun tidak boleh reassign dengan nilai baru
    ```js
     const car = {
     brand: 'civis',
     model: 'type R',
     color: 'black'
     }
     car.year=2022 //menambahkan nilai
     console.log(car);
    ```
* **Method in Object** : memasukkan value pada property yang berupa function
    ```js
     const greeting = { //tanda kurawal disebut greeting
     welcome: function() {
         return 'Halo selamat datang'
     },
     goodBye: function() {
         return 'Sampai jumpa lagi'
     }    
     }
     console.log(greeting.welcome()); // () disebut info
     console.log(greeting.goodBye());
    ```
* **Nested Object** : object yang berasalah dari turunan object lainnya
    ```js
     const bookInfo = {
     title: 'Laskar pelangi',
     year: 2005,
     author: {
         name: 'Andrea Hinata',
         age: 55,
         address: 'Bangka Belitung'
     }
     }
     console.log(bookInfo.author.age);
     console.log(bookInfo.author.address);
     console.log(bookInfo.title, bookInfo.author.name); //menampilkan hasil dalam satu line, tapi dipisahkan oleh koma
    ```
* **Looping Nested Object** : digunakan untuk mengakses data
    ```js
     for (const key in bookInfo.author) {
     console.log(bookInfo.author[key]);
     }
    ```
* **Array of Object**
    ```js
     let arr = [20, 'Salwa', 'javascript']
     let students = [{
         name: 'jessica',
         age:17,
         isVerified: true
     },
     {
         name: 'william',
         age: 18,
         isVerified: true
     },
     {
         name: 'chika',
         age: 17,
         isVerified: false
     }]
     for (const i in students) {
         console.log(students[i]); // isi keseluruhan
     let studentsName = students[i].age // looping isi age di array
         console.log(studentsName);
     }
    ``` 
> * Menyimpan banyak data pada satu variabel.
> * Pemanggilan data array dihitung dari index ke-0 (bagian paling pertama).


# GITHUB LANJUTAN
**1. Markdown**
  * Pemberian styling pada teks yang menggunakan format (.md) dalam aplikasi VS code.
  * Markdown ini memudahkan pemformatan teks tanpa penggunaan kode atau penanda yang rumit seperti di HTML.

**2. git clone**
* Untuk melakukan kontribusi ke banyak project 
* ***Pull Request*** : suatu permintaan untuk menggabungkan (merge) kode yang kita modifikasi dengan repositori utama atau repositori lain.
* Untuk dapat melakukan ***Pull request*** yg harus dilakukan : 
   - kontribusi tidak dilakukan secara langsung.
   - lakukan clone pada repository.
   - baru di push
* Langkah melakukan clone :
   - buat branch baru
      > git branch 'nama branch'
   - pindah branch gunakan command 
      > git checkout 'nama branch' / pada bagian pojok kiri bawah Code terdapat simbol branch yg bernama main / master tinggal klik dibagian situ dan pilih nama branch mana yg akan digunakan.
   - kemudian push, lalu buka repository github
   - klik button dengan tulisan "compare & pull request"
      > pastikan branch mana yg akan menerima dari branch yg lain. 
      > * ***base*** untuk menerima.
      > * ***compare*** untuk yang akan dikirimkan / dimasukkan.
   - create pull request


> cara git add dan git commit lebih mudah
> - menggunakan ***Source Control*** , dengan menggunakan itu jadi tidak perlu masuk ke dalam terminal dahulu.
> ![git add dan git commit menggunakan source control](/assets/images/source.PNG)


# JAVASCRIPT DAN HTML DOM
* DOM bukan bagian dari javascript, melaikan web API
* **Element.innerHTML** digunakan untuk
mengubah konten HTML di dalam sebuah element.
* **Element.addEventListener(“event”)** digunakan untuk menangkap interaksi user.
*  **getElementById** sering digunakan untuk membaca atau mengedit element HTML bahkan mengembalikan elemen dengan nilai tertentu.
* **getElementsByClassName** untuk mengembalikan kumpulan element dengan nama kelas yang ditentukan.