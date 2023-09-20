## Latar Belakang
Tugas mata kuliah Grafika Komputer: menggambar 3 huruf pertama dari nama panggilan menggunakan `gl.LINES` dan `gl.TRIANGLES`, dibuat animasi dengan selang waktu masing-masing 3 detik.

## Cara Kerja
### Di Fungsi main()
1. _Tag_ `script` memanggil fungsi `main` saat _window_ ter-_load_
2. Mendefinisikan `canvas`, lalu menambahkan _context_ **WebGL**
3. Menambahkan `event` saat _window_ di-_resize_
4. Deklarasi variabel untuk mengatur _frame_ (**currentFrame**) dan untuk menyimpan waktu sebelumnya (**lastTimestamp**)
5. Inisialisasi **vertexShaderSource** (untuk transformasi posisi _vertex_ di layar untuk di-_render_)
6. Pemanggilan fungsi `resizer()` untuk fitur tambahan mengubah ukuran kanvas jika _window browser_ di-_resize_
7. Pemanggilan fungsi `render()` menggunakan `requestAnimationFrame()` yang membuat fungsi memiliki variabel `timestamp`
8. Penghitungan waktu untuk mengubah nilai **currentFrame**, antara 0 dan 1, dalam milisekon
9. **currentFrame** 0 artinya menggambar menggunakan `gl.LINES`, sedangkan **currentFrame** 1 menggambar menggunakan `gl.TRIANGLES`
10. Dalam percabangan, proses yang dilakukan sama:
    a. Inisialisasi **fragmentShaderSource** untuk mendefinisikan warna dari bentuk yang akan digambar
    b. Inisialisasi **vertices** berisi titik-titik koordinat untuk menggambar
    c. Memanggil fungsi `createVertexBuffer()`
    d. Mengatur warna kanvas
    e. Mewarnai kanvas
    f. Menggambar bentuk

### Di Fungsi createVertexBuffer()
1. Memanggil fungsi `createShaderProgram()`:
    a. Meng-_compile shader vertex_ dan _fragment_
    b. Me-link program
2. Mem-_bind buffer_
3. Mendapatkan koordinat _vertices_

## Referensi
### Masukan ChatGPT
1. make me js loop that runs forever and showing the number 0 and the number 1 with the gap between them is 3 seconds
2. make me a template webgl code but put it nicely into functions
4. what is requestAnimationFrame
5. is timestamp built in?
6. does const variable in js should be initialized and cant be declared only?

### Video
1. [Mengubah ukuran kanvas](https://www.youtube.com/watch?v=2MWBDHOEdEU&list=PLPqKsyEGhUnaOdIFLKvdkXAQWD4DoXnFl&index=11&ab_channel=DavidParker)