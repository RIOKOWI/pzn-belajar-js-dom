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