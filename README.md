# Laravel 10 + Restful API
## Required
- cek composer : `composer`

- Jika belum ada, maka instal composer terlebih dahulu

## Installation laravel
- install project laravel : `composer create-project --prefer-dist laravel/laravel:^10.0 laravel10-api`
- masuk ke folder : `cd laravel10-api`
- test jalankan : `php artisan serve`

## Result
Hasilnya akan tampil seperti dibawah
![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/7428353a-c44b-413b-8723-e7313719f6db)

## Persiapan untuk data 
- untuk membuat folder penyimpanan data : `php artisan storage:link`, hasil menjadi folder public `storage/app/public`
- buat file API Reource : `php artisan make:resource PostResource`, hasil akan membuat folder `resource` dan file `PostResource.php`
- create db on server : contoh nama db `db_laravel10_api`
- edit config db : edit file `.env` sesuaikan dengan setingan db masing-masing,
  contoh :
  ```bash
  DB_DATABASE=db_laravel10_api
  DB_USERNAME=root
  DB_PASSWORD=
  ```
- buat model post dan migrations : `php artisan make:model Post -m`, hasil akan generate file model dan migrasi `app/Models/Post.php` dan `database/migrations/tanggal_sekarang-create-post-table.php`
- migrasi semua data : `php artisan migrate`, file pada folder `database/migrations` akan di migrasikan semua (server harus keadaan nyala dan terkoneksi dengan db)
- membuat controller post : `php artisan make:controller Api/PostController`
- cek route : `php artisan route:list`

- kirim data menggunakan aplikasi postman mengunakan methode `POST` : `http://localhost:8000/api/posts`, klik send pada kanan atas seperti gambar dibawah
  ![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/87b50579-918c-48ea-9541-ba71755ff6e6)
  image : file, title : text, content : text, value sesuaikan kebutuhan

  Hasil send data
  ![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/0f52d581-f74c-4233-9aee-275a3f158be8)

  Cek hasil senda data pada browser
  `http://localhost:8000/api/posts/1`
  ![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/cdbec66f-58bd-4dc6-8b58-0a39e9524d58)

  Jika menggunakan postman maka methode menggunakan `GET`
  ![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/9b373f4f-7941-4bfa-84bc-f724cfb7343e)



# Laravel 10 + Vue.js 3
Laravel v.10 + VueJs v.3

## Required
- Cek versi nodejs : `node --version`
- Cek versi npm : `npm --version`

- Jika belum terinstal, maka harus instal terlebih dahulu

## Installation
- install template vue : `npm create vite@4.2.0 vue3-crud -- --template vue`
- masuk ke project : `cd vue3-crud`
- install npm ke dalam project : `npm install`
- coba jalankan : `npm run dev`

## Result
Hasilnya akan tampil seperti dibawah
![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/afe64c24-4f43-41ba-ae9e-32edced724ca)


## Install Vue Router
- Install vue router : `npm install vue-router@4.1.6`\
- Add bootstrap : `index.html`
```bash
  <head>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
  </head>
```
```bash

  <body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
  </body>
```

## Install Axios untuk konek API
- Instal library : `npm install axios@1.3.4`

# Result Project
Untuk menggunakan vuejs pastikan server API (laravel/backend sedang berjalan) dan server db pastikan berjalan karena repository [Laravel 10 + Vue Js 3](https://github.com/omeans-team/laravel10-vuejs3) ini menggunakan database
![image](https://github.com/omeans-team/installation-vuejs/assets/47584746/3c52faa8-04c8-4d1a-ac3c-ebc90d58c403)


## Frontend
This link for repository result Vue Js [Laravel 10 + Vue Js 3](https://github.com/omeans-team/laravel10-vuejs3)
## Backend
This link for repository result Laravel Api [Laravel 10 + Restful API](https://github.com/omeans-team/laravel10-api)
