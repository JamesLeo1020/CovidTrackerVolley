# CovidTrackerVolley
Rest API Volley ini menggunakan data dari https://corona.lmao.ninja/v2/all

referensi https://www.section.io/engineering-education/making-api-requests-using-volley-android/

![Alt Text](https://github.com/leo-chan1020/CovidTrackerVolley/blob/master/Screenshot_20210510-213835_CovidTrackerVolley.jpg)

Jelaskan Perbedaan dari penggunaan Retrofit dan Volley!

Retrofit merupakan library android yang dibuat oleh Square yang digunakan sebagai REST Client pada Android, yang pasti akan memudahkan kita. Karena kita tidak perlu lagi untuk membuat method-method sendiri untuk menggunakan REST Client API dari backend. Library ini menyediakan framework yang powerfull untuk authenticating dan berinteraksi dengan API dengan mengirimkan request menggunakan OkHTTP

Volley
Volley merupakan produk yang diperkenalkan oleh Google untuk mempermudah pertukaran data tanpa harus membuat deretan kode yang sangat panjang. Secara default volley menggunakan metode singkronisasi jadi anda tidak perlu membuat sebuah method atau fungsi yang menggunakan class asynctask.
Melakukan sebuah request queuing and prioritization (Mengutamakan prioritas dalam sebuah antrian)

Sangat efektif untuk melakukan chace dan efesiensi penyimpanan (memory)
Dapat melakukan perubahan class sesuai dengan kebutuhan
Dapat melakukan pembatalan dalam sebuah request.
Teman-teman bingung akan menggunakan library mana ketika membuat aplikasi android?
Gunakan Retrofit jika teman-teman mendevelop aplikasi yang menggunakan REST API standar dengan json response dan tidak terlalu banyak custom requirement dalam caching, Requenst Priority, retries, dll. Volley jika anda membutuhkan fleksibelitas dalam network layer anda.
Berikut adalah perbandingan Retrofit dan Volley secara detail:
Mudah digunakan
Retrofit : Retrofit sangat mudah digunakan. Memungkinkan anda untuk memakai API ini dengan method sederhana dari java menggunakan interface.
Volley : Sedikit lebih rumit pada umumnya. Volley hanya mendukung beberapa response yaitu String,Image,JSONObject dan JSONArray.
Performan dan Caching
Retrofit : Caching harusnya bisa berjalan jika server anda menetapkan header control yang benar. Jika tidak ,atau anda melakukan sesuatu yang tidak biasa anda hanya bisa mengubah lapisan klien Http anda.
**Volley **: Volley memiliki mekasnisme chacing yang lebih rumit dan fleksibel, memanfaatkan untuk membuat caching bitmaps yang lebih besar.
POST requests + multipart uploads
Retrofit : memiliki dukungan penuh untuk permintaan POST dan upload file yang multi, dengan API Sweet untuk boot.
Volley: support POST request tetapi anda harus convert terlebih dahulu java objek yang kita buat menjadi JSONObject.
