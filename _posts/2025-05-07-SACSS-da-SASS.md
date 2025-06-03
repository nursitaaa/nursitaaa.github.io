---
layout: post
title: "SACSS dan SCSS"
---

berikut adalah penjelasan tentang SACSS dan SCSS.

### Pengertian Dari SASS
SASS merupakan praprosesor dari CSS yang digunakan sebagai alat pengembang oleh developer untuk menulis kode CSS dengan menggunakan fitur yang lebih canggih, yaitu dengan menggunakan variabel atau pewarisan untuk mempermudah pemeliharaan kode. Kepanjangan dari SASS merupakan Syntacticakky Awesome Style Sheets.  

Jadi SASS adalah bahasa yang akan membuat CSS, dan SASS juga akan memberikan fitur yang tidak dimiliki CSS. Salah satunya fitur yang digunakan untuk menulis kode agar lebih bersih dan juga rapih, dan dapat menghindari penulisan kode yang berulang. Untuk fungsi SASS yang paling utama adalah untuk membantu Anda mengurangi jumlah kode yang harus ditulis.  

### Fitur yang Ada Dalam SASS
Berikut merupakan fitur SASS yang dapat Anda gunakan dalam pekerjaan sehari-hari:  

# Variable
Penggunaan variable dalam SASS, yang memiliki fungsi seperti variable dalam bahasa pemrograman lain yang bisa digunakan berulang kali atau bahkan bisa dipanggil oleh fungsi-fungsi lain. Variable yang ada pada SASS menggunakan lambang $.  

    contoh :
    ```
        $font-stack: Helvetica, sans-serif;
    $main-color: #333;

    body {
    font-family: $font-stack;
    color: $main-color;
    }
    ```

# Nesting Selector
Ketika di CSS mungkin Anda sering menulis selector yang sama berulang kali. Namun dalam SASS Anda tidak perlu menggunakan penulisan selector yang sama berulang kali, berkat adanya nesting selector.  

     contoh :
     ```

     nav {
  ul {
    li {
      a {
        color: white;
      }
    }
  }
}

```

# Import
SASS dapat memecah salah satu file CSS ke dalam beberapa file SASS dengan skala yang lebih kecil, namun masih tetap bisa di compile menjadi file CSS. Hal ini sangat berguna bagi Anda untuk menjaga kode tetap terbaca dengan line of code dalam satu file.  

    contoh :

    ```
    // main.scss
    @import 'colors';
    ```

# Partial
Dalam fitur pada SASS partial disebut dengan file yang kecil dan juga dapat diimport ke file SASS lainnya.  

   contoh :
    ```
     // _colors.scss
     $primary: #f00;
     ```

# Mixin
Mixin merupakan salah satu fitur yang dapat mengakomodir keinginan Anda. Mixin juga dapat membuat satu fungsi yang nantinya dapat dipakai di tempat lain.  

     contoh :
     ```
     @mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  @include flex-center;
}

```


# Placehorder
Fitur placehorder berguna ketika Anda ingin menulis dengan gaya yang tidak menggunakan gaya CSS dasar, tetapi menggunakan gaya CSS yang terbaru.  

   contoh :
   ```
   %button-base {
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: bold;
}

.btn-primary {
  @extend %button-base;
  background-color: blue;
  color: white;
}

.btn-secondary {
  @extend %button-base;
  background-color: gray;
  color: black;
}

```

# Kondisional
SASS dapat menggunakan fitur kondisional berdasarkan variable yang di assign.  

   contoh :
   ```
   $theme: dark;

body {
  @if $theme == light {
    background-color: white;
    color: black;
  } @else if $theme == dark {
    background-color: black;
    color: white;
  } @else {
    background-color: gray;
    color: white;
  }
}
```

# Perulangan
Ketika Anda ingin melakukan SASS, Anda bisa menggunakan for maupun while, dan selain itu SASS juga dapat melakukan pengulangan menggunakan @peach.  contoh :
1. @for Loop
```
@for $i from 1 through 5 {
  .mt-#{$i} {
    margin-top: 10px * $i;
  }
}
```
Output :

```
.mt-1 { margin-top: 10px; }
.mt-2 { margin-top: 20px; }
... dan seterusnya
```
2. @while Loop
```$i: 1;

@while $i <= 3 {
  .mb-#{$i} {
    margin-bottom: $i * 5px;
  }
  $i: $i + 1;
}
```
3. @each Loop
```$colors: red, green, blue;

@each $color in $colors {
  .text-#{$color} {
    color: $color;
  }
}
```

### Bagaimana Cara Kerja Dari SASS?
Cara kerja SASS sama halnya dengan menggunakan bahasa pemrograman, SASS harus dikompilasikan terlebih dahulu untuk menggunakannya. Dari hasil kompilasi tersebut SASS akan berubah menjadi file CSS. File CSS inilah yang dapat digunakan pada web. 

Proses tersebut disebut dengan transpiling. Dalam proses transpiling Anda hanya perlu memberikan beberapa kode SASS kepada transpiler (seseorang yang menggunakan pemrograman) untuk mendapatkan kembali beberapa kode CSS.  

SASS menggunakan persyaratan sistem tertentu yaitu sistem operasi, sistem operasi SASS adalah platform yang independen. Dengan adanya dukungan browser, SASS akan berfungsi di Edge/IE (dari IE 8), Firefox, Chrome, Safari, Opera dan sistem bahasa pemrograman SASS didasarkan pada bahasa ruby.  

### Kelebihan Dalam SASS
Berikut merupakan kelebihan SASS yang perlu Anda ketahui: 

1. Dapat digunakan kembali
Keuntungan menggunakan SASS adalah dapat menyediakan cara bagi pengembang untuk mengatur stylesheet ke dalam file individual dan juga parsial, yang bertujuan agar kode mudah terbaca, dipelihara, dan juga digunakan kembali.  

2. Adanya aturan Import SASS
Aturan import SASS akan menggabungkan file kode kecil menjadi besar, serta membantu memisahkan serta mengatur kode, sehingga mudah dipelihara dan dibaca.  

Untuk secara keseluruhannya aturan import SASS akan membantu dalam membedakan CSS konvensional dengan menyediakan cara yang intuitif dan juga efisien. Hal tersebut bertujuan guna mengatur dan memisahkan kode sekaligus membantu mengurangi kecepatan manual halaman.  

3. Dapat Menyimpan Variabel
Ketika menggunakan SASS akan dapat menyimpan variabel di satu tempat, sehingga seluruh aplikasi atau web dapat mengaksesnya. Dengan adanya variabel dapat digunakan untuk menyimpan nilai warna, ukuran, font, margin, dan lain sebagainya.  

4. Dapat menyarangkan penyeleksian
Ketika menggunakan SASS Anda dapat menyarangkan penyeleksi antara satu sama lain untuk membuat kode yang lebih terorganisir dan juga dapat menyederhanakan rantai pemilih yang kompleks.  

### Perbedaan SASS dengan SCSS
Antara SASS dengan SCSS sebetulnya memiliki tujuan yang sama, hanya yang membedakannya ada pada bagian kepenulisan dan juga penggunaannya. Berikut merupakan perbedaan SASS dan SCSS.  

Apabila Anda menggunakan SCSS, maka Anda perlu membuat sebuah file dengan berekstensikan SCSS, dan untuk menggunakan SASS Anda perlu membuat file tersebut dengan berekstensikan. 

Untuk perbedaan utama dan paling menonjol antara SASS dengan SCSS terletak pada penulisannya dimana SCSS menggunakan kurung kurawal seperti CSS lainnya. Sedangkan untuk SASS menggunakan identitas Python.  

Untuk perbedaan utamanya selanjutnya SASS dengan SCSS yaitu:  

- SASS digunakan ketika membuat sintaks kode yang asli, sedangkan SCSS tidak membutuhkan sintaks kode.  
- SASS mengikuti lekukan yang ketat, sedangkan SCSS tidak mengikuti lekukan ketat.  
- SASS memiliki lebih banyak komunitas dibandingkan SCSS.  
- SASS tidak dapat digunakan sebagai CSS dan begitu juga sebaliknya.  
-  SASS akan sulit ditambahkan ke proyek CSS yang sudah ada, sedangkan SCSS dapat ditambahkan dengan mudah ke proyek CSS yang sudah ada.  