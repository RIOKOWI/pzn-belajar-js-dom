# SLIDE
- `https://docs.google.com/presentation/d/1f8N--iCqI8iQ9RS4LijVBqTLNd40XHhPi-TeSRVcpSs/`


# JavaScript Document Object Model

# Pengenalan Document Object Model
## Pengenalan Document Object Model
- Ketika sebuah website di load oleh Browser, maka Browser akan membuat Document Object Model untuk halaman website tersebut
- DOM dibuat dalam bentuk tree / pohon yang tiap cabang nya berisikan object dari jenis elemen HTML
- JavaScript memiliki kemampuan untuk memanipulasi DOM, artinya dengan JavaScript, kita bisa mengakses tiap object di DOM bahkan memanipulasi object nya

## Diagram DOM
`https://docs.google.com/presentation/d/1f8N--iCqI8iQ9RS4LijVBqTLNd40XHhPi-TeSRVcpSs/edit?slide=id.gf5a4e9fac3_0_5#slide=id.gf5a4e9fac3_0_5`


## DOM dan JavaScript
- DOM bukanlah fitur atau bahasa pemrograman, DOM sebenarnya hanyalah representasi Object dari Struktur halaman web
- DOM sendiri sebenarnya bukanlah bagian dari bahasa pemrograman JavaScript, melainkan bagian dari Web API
- DOM sendiri di desain secara agnostik, artinya sebenarnya bisa digunakan menggunakan bahasa pemrograman apapun, karena memang untuk membuat Web, kita tidak hanya bisa menggunakan bahasa pemrograman JavaScript


# Tipe Data
## Tipe Data
- DOM memiliki representasi data
- Tidak terlalu banyak tipe data yang terdapat di DOM
- Oleh karena itu, sebenarnya DOM sangat sederhana, namun penggunaannya sangat bermanfaat

| Tipe Data | Keterangan |
|---|---|
| `Document` | Merupakan representasi dari halaman web |
| `Node` | Merupakan base class untuk semua tipe data di DOM, seperti Document, Element, dan Attr |
| `Element` | Merupakan representasi object element di halaman web, misal head, body, form, input, dan lain-lain |
| `NodeList` | Merupakan array/collection yang berisikan Node |
| `Attr` | Atau attribute, merupakan representasi object attribute dalam element |
| `NamedNodeMap` | Merupakan collection yang berisikan Attr dalam bentuk Map |


# Document
## Document
- Document merupakan representasi object dari halaman web
- Dalam satu halaman web, terdapat satu document, dan kita tidak perlu membuatnya secara manual, karena otomatis akan ada di browser
- Untuk mengakses Document, kita bisa gunakan object document
- `https://developer.mozilla.org/en-US/docs/Web/API/Document`


## Document Object
- Document secara otomatis dibuat dalam browser ketika membuka halaman web, sehingga kita tidak perlu membuat objek Document secara manual
- Kita bisa langsung menggunakan kata kunci document


## Document Property
- Document memiliki banyak sekali property
- Property dalam Document bisa kita gunakan untuk melihat semua data yang terdapat dalam document halaman web
- `https://developer.mozilla.org/en-US/docs/Web/API/Document#properties`

## Document Method
- Document memiliki banyak sekali method
- Banyak method yang terdapat di document digunakan untuk memanipulasi data DOM, misal membuat Node, Element, Attribute atau mengambil dan menyeleksi Node di dalam document
- `https://developer.mozilla.org/en-US/docs/Web/API/Document#methods`


contoh di file :
- `document.html`
- `document-property.html`
- `document-method.html`

# Node
## Node
- Node adalah base class dari Document, Element dan Attr
- Artinya semua fitur yang dimiliki di Node dimiliki diturunannya
- Node dalam DOM itu bentuknya adalah Tree (pohon), artinya dengan Node, kita bisa melihat Parent (node diatas nya), Children (node dibawahnya), Sibling (node disebelahnya)
- `https://developer.mozilla.org/en-US/docs/Web/API/Node`


## Node Property
- Node memiliki banyak sekali property
- Property di Node banyak berisi informasi reference ke Node lain nya, seperti ke node parent nya, node children nya atau node sebelahnya
- `https://developer.mozilla.org/en-US/docs/Web/API/Node#properties`


## Node Method
- Node memiliki banyak sekali method
- Method di Node bisa digunakan untuk memanipulasi data Node di dalam Node tersebut, misal menambah/menghapus Node children
- `https://developer.mozilla.org/en-US/docs/Web/API/Node#properties`


contoh di file :
- `node.html`
- `node-props.html`
- `node-method.html`


# Element
## Element
- Element merupakan Node yang berbentuk element, biasanya adalah element HTML, misal <html>, <head>, <body>, <div>, <table>, dan lain-lain
- `https://developer.mozilla.org/en-US/docs/Web/API/Element`

## Element Property
- Element memiliki banyak sekali property
- Dan karena Element adalah turunan dari Node, semua property Node pun bisa digunakan di Element
- `https://developer.mozilla.org/en-US/docs/Web/API/Element#properties`

## Element Method
- Element memiliki banyak sekali method
- Dan karena Element adalah turunan dari Node, semua method Node pun bisa digunakan di Element
- `https://developer.mozilla.org/en-US/docs/Web/API/Element#methods`


## Membuat Element
- Sebelumnya kita hanya mengambil element menggunakan id, artinya kita perlu buat dulu element nya di HTML
- Kita juga bisa membuat object element baru, dan menambahkannya ke halaman web
- Kita bisa menggunakan method createElement(tag) pada Document
- `https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement`


contoh di file :
- `element.html`
- `element-property.html`
- `create-element.html`

# NodeList
## NodeList
- NodeList adalah kumpulan dari Node
- Biasanya NodeList digunakan ketika kita menyeleksi banyak Node sekaligus, misal ketika kita ingin mengambil semua children di Node misalnya
- `https://developer.mozilla.org/en-US/docs/Web/API/NodeList`

## Live vs Static NodeList
- NodeList memiliki 2 tipe, yaitu Live dan Static
- Live artinya perubahan yang terjadi pada NodeList nya, akan merubah semua NodeList yang sama
- Static artinya perubahan yang terjadi pada NodeList nya, tidak akan merubah semua NodeList yang sama
- Saat kita menggunakan element.childNodes, NodeList tersebut bersifat Live
- Saat kita menggunakan document.querySelectorAll(), NodeList tersebut bersifat Static

contoh di file :
- `node-list.html`
- `live-nodelist.html`
- `static-nodelist.html`

# Attr
## Attr
- Attr atau attribute merupakan representasi dari attribute sebuah element, atau singkatnya key-value, key nya adalah nama attribute, dan value nya adalah value attribute
- `https://developer.mozilla.org/en-US/docs/Web/API/Attr`

## Attr Value
- Kadang kebanyakan programmer ingin langsung mendapatkan value Attr 
- Jarang sekali menggunakan object Attr nya
- Untuk mendapatkan value secara langsung, kita bisa menggunakan method getAttribute(name) di Element

## Membuat Attr
- Untuk membuat Attr, kita bisa menggunakan document.createAttribute(name)
- Lalu untuk menambahkannya ke Element, kita bisa gunakan element.setAttributeNode(attr)
- Atau kita juga bisa langsung membuat Attr langsung dengan name dan value nya menggunakan element.setAttribute(name, value)

contoh di file :
- `attr.html`
- `attr-value.html`
- `create-attr.html`

# NamedNodeMap
## NamedNodeMap
- NamedNodeMap merupakan kumpulan dari Attr
- Mirip seperti NodeList, namun isinya adalah Attr
- `https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap`

contoh di file :
- `node-map.html`

# Text Node
## Text Node
- Saat kita membuat HTML, kadang kita membuat teks tanpa tag
- Saat halaman web tersebut direpresentasikan dalam DOM, text tanpa tag bukanlah merupakan Element, melainkan Node
- Lebih tepatnya adalah Text Node
- `https://developer.mozilla.org/en-US/docs/Web/API/Text`

## Membuat Text Node
- Kita juga bisa membuat Text Node menggunakan method document.createTextNode(string)
- Hasilnya berupa Text yang bisa kita tambahkan ke Node lain

contoh di file :
- `text-node.html`
- `create-text-node.html`

# Event Handler
## Event Handler
- Node memiliki kemampuan bereaksi terhadap suatu kejadian, misal kejadian di klik, mouse di atas node tersebut, dan lain-lain
- Ada banyak sekali jenis kejadian yang bisa kita buatkan aksinya ketika kejadian tersebut terjadi, atau dikenal dengan nama Event Handler
- Ada dua cara kita menambahkan Event Handler ke Node, menggunakan Event Target atau Global Event Handler
- `https://developer.mozilla.org/en-US/docs/Web/API/EventTarget`
- `https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers`


## Event Target
- Event Target merupakan parent class dari Node, artinya semua Node memiliki kemampuan dari Event Target
- Pada Event Target, kita bisa menggunakan method addEventListener(type, callback) untuk menambahkan Event Handler
- `https://developer.mozilla.org/en-US/docs/Web/API/EventTarget`

## Global Event Handler
- Selain menggunakan Event Target, untuk menambahkan Event Handler, kita juga bisa menggunakan Global Event Handler
- Global Event Handler bukanlah sebuah super class, hanya kontrak yang bisa kita gunakan untuk menambah event handler sesuai dengan type event nya
- `https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers`

* bedanya addevent listener biasa dan global event handler adalah yang biasa bisa menambahkan listener lebih dari 1

contoh di file :
- `event-listener.html`

# Event
## Jenis Event
- DOM sendiri memiliki banyak sekali jenis event, tidak hanya click
- Jenis event yang bisa kita gunakan biasanya disesuaikan dengan target event nya, misal pada element video, ada event play, pause, sedangkan pada element button, tidak ada event play atau pause
- Untuk lebih detailnya, ada apa saja jenis event nya, kita bisa lihat pada halaman berikut :
- `https://developer.mozilla.org/en-US/docs/Web/Events`

## Event
- Saat kita membuat callback function untuk Event Handler, kita juga bisa menerima data event yang memicu event itu terjadi
- Data Event tersebut bisa berbeda-beda, tergantung jenis Event nya, contohnya untuk Click, data event nya berupa Mouse Event (yang berisi lokasi mouse dan lain-lain)
- Kita bisa lihat detail dari data tiap event di halaman documentation nya :
- `https://developer.mozilla.org/en-US/docs/Web/API/Event`

contoh di file :
- `event.html`

# Style
## Style
- DOM juga bisa digunakan untuk memanipulasi attribute style pada element dengan lebih mudah
- Kita tidak perlu menggunakan setAttribute(“style”, “value”) setiap ingin mengubah style sebuah element
- Kita bisa langsung gunakan element.style.name = value
- `https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style`


## Nama Style
- Saat kita mengubah sebuah style, penamaan style menjadi berubah
- Pada style css, rata-rata menggunakan format lowercase dan -, misal background-color
- Sedangkan pada DOM Style, menggunakan format pascalCase, misal backgroundColor

contoh di file :
- `style.html`

# InnerText dan InnerHTML
## InnerText dan InnerHTML
- Selain textContent, terdapat property lain bernama innerText untuk mendapatkan isi text sebuah element
- Tujuan nya sama, untuk mengambil atau mengubah isi text konten sebuah element, namun ada perbedaannya
- textContent akan mengembalikan semua isi dari konten text sebuah element
- innerText bisa tahu, bagian text mana yang ditampilkan, dan dia hanya akan mengambil text yang ditampilkan saja

## Inner HTML
- Jika Text Content dan Inner Text hanya mengambil text saja, Inner HTML akan mengambil seluruh element HTML nya sebagai text
- Ini juga cocok jika kita ingin mengubah isi dari element menggunakan text yang berisi tag HTML

## Mengubah Element dengan Inner HTML
- Salah satu kemampuan dari innerHTML adalah, kita bisa mengubah isi dari children sebuah element hanya dengan string 
- Tag yang terdapat di dalam String secara otomatis akan menjadi child element

contoh di file :
- `text-inner-content.html`


# Window
## Window
- Window merupakan representasi window yang berisikan DOM Document
- Beberapa JavaScript function sebenarnya berasal dari object Window, seperti alert(), confirm() dan prompt()
- Ada banyak sekali property, method  dan event yang bisa kita gunakan pada window
- Untuk menggunakan Window, kita tidak perlu membuat objectnya, cukup gunakan kata kunci window
- `https://developer.mozilla.org/en-US/docs/Web/API/Window`


contoh di file :
- `wiindow.html`

# Query Selector
## Query Selector
- Sebelumnya kita sudah menggunakan method querySelectorAll() pada Document, sekarang kita akan bahas lebih lengkap tentang Query Selector
- Query Selector merupakan method untuk menseleksi node sesuai dengan pola yang kita ingin cari
- Terdapat dua method untuk Query Selector :
  - Document.querySelector(pola) digunakan menyeleksi node pertama yang sesuai dengan pola
  - Document.querySelectorAll(pola) digunakan untuk menyeleksi semua node yang sesuai dengan pola


## Pola Query Selector
- Pola untuk Query Selector adalah menggunakan CSS Selector
- Penggunakan Pola nya mirip ketika kita membuat Selector di CSS
- Jika belum tahu tentang CSS Selector, disarankan untuk dipelajari ulang tentang materi CSS
- `https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors`

## Universal Selector
- Universal Selector merupakan selector untuk menyeleksi semua element
- Kita bisa menggunakan karakter *
- `https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors`

## Type Selector
- Type Selector adalah selector yang digunakan untuk menyeleksi  tag type HTML yang kita pilih
- Untuk menggunakannya, kita bisa langsung sebutkan nama tag nya
- `https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors`

## Class Selector
- Class Selector merupakan selector untuk menyeleksi semua element yang memiliki class yang sesuai selector
- Untuk menggunakannya, kita bisa sebutkan nama class nya diawali dengan titik
- `https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors`

contoh di file :
- `universal-selector.html`
- `type-selector.html`