# BAB 1: PENGENALAN PEMROGRAMAN DAN C++

**Mata Kuliah:** Dasar-Dasar Pemrograman  
**Kode:** DDP101  
**Pertemuan:** 01 (Minggu 1)  
**Bobot:** 3 SKS (2 SKS Teori + 1 SKS Praktikum)

---

## CAPAIAN PEMBELAJARAN

Setelah mempelajari bab ini, mahasiswa diharapkan mampu:

1. Menjelaskan konsep dasar pemrograman dan paradigma pemrograman
2. Mendeskripsikan sejarah dan karakteristik bahasa C++
3. Memahami struktur dasar program C++
4. Menjelaskan proses kompilasi dan eksekusi program
5. Menginstal dan mengkonfigurasi IDE Code::Blocks
6. Menulis, mengkompilasi, dan menjalankan program C++ sederhana
7. Mengidentifikasi dan memperbaiki kesalahan kompilasi dasar

---

## 1.1 KONSEP DASAR PEMROGRAMAN

### 1.1.1 Apa itu Pemrograman?

Pemrograman adalah proses merancang dan menulis instruksi-instruksi yang dapat dieksekusi oleh komputer untuk menyelesaikan suatu masalah atau mencapai tujuan tertentu. Dalam konteks pertahanan, pemrograman memungkinkan kita membuat sistem informasi militer, aplikasi monitoring peralatan, hingga sistem command-and-control yang kompleks.

Bayangkan seorang komandan yang memberikan perintah kepada pasukannya. Perintah tersebut harus jelas, terstruktur, dan tidak ambigu. Sama halnya dengan pemrograman—kita memberikan instruksi kepada komputer dalam bahasa yang dapat dipahaminya.

> **Definisi:** Pemrograman adalah seni dan sains merancang solusi algoritmik untuk masalah, kemudian mengimplementasikan solusi tersebut dalam bahasa pemrograman yang dapat dieksekusi oleh komputer.

### 1.1.2 Komponen Utama Pemrograman

Setiap program komputer pada dasarnya terdiri dari tiga komponen utama:

1. **Input (Masukan)** - Data yang diterima program dari pengguna, file, sensor, atau sumber lainnya
2. **Process (Proses)** - Pengolahan data menggunakan algoritma dan logika tertentu
3. **Output (Keluaran)** - Hasil yang dihasilkan program, bisa berupa tampilan di layar, file, atau aksi lainnya

Dalam konteks militer, contohnya:
- **Input**: Data posisi GPS prajurit
- **Process**: Menghitung jarak antar unit, analisis formasi
- **Output**: Peta taktis dengan posisi semua unit

### 1.1.3 Algoritma dan Flowchart

Sebelum menulis kode program, seorang programmer harus merancang algoritma terlebih dahulu. Algoritma adalah urutan langkah-langkah logis untuk menyelesaikan masalah.

> **Definisi:** Algoritma adalah urutan langkah-langkah yang terdefinisi dengan baik, terbatas, dan tidak ambigu untuk menyelesaikan suatu masalah.

Karakteristik algoritma yang baik:
- **Finite (Terbatas)**: Memiliki awal dan akhir yang jelas
- **Definite (Pasti)**: Setiap langkah tidak ambigu
- **Input**: Memiliki 0 atau lebih masukan
- **Output**: Menghasilkan minimal 1 keluaran
- **Effective**: Setiap langkah dapat dikerjakan

Flowchart adalah representasi visual dari algoritma menggunakan simbol-simbol standar.

![Simbol Flowchart Dasar](images/p01-01-flowchart-symbols.png)

*Gambar 1.1: Simbol-simbol standar dalam flowchart*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Standard flowchart symbols chart showing 6 basic symbols with labels
STYLE: Clean flat vector illustration, educational diagram, textbook quality, minimal design
LAYOUT: Grid layout, 2 columns x 3 rows
COLORS: 
- Primary: #2563eb (blue) for symbols
- Secondary: #10b981 (green) for arrows
- Text: #1f2937 (dark gray)
- Background: #ffffff (white)
ELEMENTS:
1. Terminator (oval): top-left, with "Mulai/Selesai" label
2. Process (rectangle): top-right, with "Proses" label
3. Decision (diamond): middle-left, with "Keputusan" label
4. Input/Output (parallelogram): middle-right, with "Input/Output" label
5. Arrow (line with arrowhead): bottom-left, with "Alur" label
6. Connector (small circle): bottom-right, with "Konektor" label
LABELS: All text in Bahasa Indonesia, clear sans-serif font
SIZE: 800x600 pixels
FORMAT: PNG, white background
NEGATIVE: No gradients, no 3D effects, no photorealistic elements
```

---

### SOLVED PROBLEM 1.1 ⭐

**Soal:** Buatlah algoritma untuk menghitung luas persegi panjang jika diketahui panjang dan lebar.

**Penyelesaian:**

**Algoritma:**
```
1. Mulai
2. Baca nilai panjang
3. Baca nilai lebar
4. Hitung luas = panjang × lebar
5. Tampilkan luas
6. Selesai
```

**Flowchart:**

![Flowchart Luas Persegi Panjang](images/p01-02-flowchart-rectangle.png)

*Gambar 1.2: Flowchart algoritma menghitung luas persegi panjang*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Flowchart diagram for calculating rectangle area
STYLE: Clean flat vector illustration, educational diagram, textbook quality
LAYOUT: Vertical flow from top to bottom
COLORS: 
- Terminator: #10b981 (green)
- Process: #2563eb (blue)
- Input/Output: #f59e0b (orange)
- Arrows: #6b7280 (gray)
- Background: #ffffff (white)
ELEMENTS:
1. Oval "Mulai": top center
2. Parallelogram "Input: panjang, lebar": below Mulai
3. Rectangle "luas = panjang × lebar": below Input
4. Parallelogram "Output: luas": below Process
5. Oval "Selesai": bottom center
6. Arrows connecting all elements downward
LABELS: All text in Bahasa Indonesia
SIZE: 600x800 pixels
FORMAT: PNG, white background
NEGATIVE: No gradients, no complex shadows
```

---

### SOLVED PROBLEM 1.2 ⭐

**Soal:** Buatlah algoritma untuk menentukan apakah seorang prajurit lolos seleksi fisik. Syarat lolos: lari 12 menit minimal 2400 meter DAN pull-up minimal 8 kali.

**Penyelesaian:**

**Algoritma:**
```
1. Mulai
2. Baca jarak_lari (dalam meter)
3. Baca jumlah_pullup
4. Jika (jarak_lari >= 2400) DAN (jumlah_pullup >= 8) maka
     Tampilkan "LOLOS"
   Jika tidak
     Tampilkan "TIDAK LOLOS"
5. Selesai
```

**Penjelasan:** Algoritma ini menggunakan operator logika AND karena KEDUA syarat harus terpenuhi. Jika salah satu syarat tidak terpenuhi, prajurit dinyatakan tidak lolos.

---

## 1.2 PARADIGMA PEMROGRAMAN

### 1.2.1 Apa itu Paradigma Pemrograman?

Paradigma pemrograman adalah cara pandang atau pendekatan dalam menulis program. Berbagai paradigma memberikan filosofi berbeda tentang bagaimana masalah harus dipecahkan dan bagaimana program harus distruktur.

![Paradigma Pemrograman](images/p01-03-programming-paradigms.png)

*Gambar 1.3: Berbagai paradigma pemrograman utama*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Programming paradigms comparison diagram showing 4 main paradigms
STYLE: Clean flat vector illustration, educational infographic, modern design
LAYOUT: 2x2 grid layout with central title
COLORS: 
- Procedural: #2563eb (blue)
- OOP: #10b981 (green)
- Functional: #f59e0b (orange)
- Logic: #8b5cf6 (purple)
- Background: #ffffff (white)
ELEMENTS:
1. Center title: "PARADIGMA PEMROGRAMAN"
2. Top-left box: Icon of sequential steps + "Prosedural" label
3. Top-right box: Icon of objects/classes + "Berorientasi Objek (OOP)" label
4. Bottom-left box: Icon of mathematical function + "Fungsional" label
5. Bottom-right box: Icon of logic gates + "Logika" label
6. Each box has 2-3 bullet points of characteristics in Indonesian
LABELS: All text in Bahasa Indonesia
SIZE: 800x600 pixels
FORMAT: PNG, white background
NEGATIVE: No gradients, no 3D effects
```

### 1.2.2 Pemrograman Prosedural

Pemrograman prosedural adalah paradigma yang paling mendasar dan mudah dipelajari. Program ditulis sebagai urutan prosedur atau fungsi yang dieksekusi secara berurutan.

**Karakteristik:**
- Fokus pada prosedur/fungsi
- Eksekusi berurutan (top-to-bottom)
- Data dan fungsi terpisah
- Cocok untuk program sederhana hingga menengah

**Contoh bahasa:** C, Pascal, FORTRAN, dan C++ (untuk pemrograman prosedural)

**Analogi militer:** Seperti SOP (Standard Operating Procedure) yang berisi langkah-langkah berurutan untuk menjalankan suatu operasi.

### 1.2.3 Pemrograman Berorientasi Objek (OOP)

OOP mengorganisir program sebagai kumpulan objek yang berinteraksi. Setiap objek memiliki data (atribut) dan perilaku (method).

**Karakteristik:**
- Fokus pada objek dan class
- Enkapsulasi data dan fungsi
- Inheritance (pewarisan)
- Polymorphism (polimorfisme)

**Contoh bahasa:** Java, Python, C++, C#

**Analogi militer:** Seperti organisasi militer dengan berbagai unit (Infantry, Cavalry, Artillery) yang merupakan spesialisasi dari class induk "Pasukan", masing-masing punya atribut dan kemampuan berbeda.

### 1.2.4 Pemrograman Fungsional

Pemrograman fungsional memperlakukan komputasi sebagai evaluasi fungsi matematis dan menghindari perubahan state.

**Karakteristik:**
- Fungsi adalah first-class citizens
- Immutability (data tidak berubah)
- Pure functions (tidak ada side effects)
- Recursion lebih diutamakan daripada loops

**Contoh bahasa:** Haskell, Lisp, Erlang, Scala

### 1.2.5 C++ dan Multi-Paradigma

C++ adalah bahasa **multi-paradigma**. Artinya, C++ mendukung berbagai paradigma pemrograman:

1. **Prosedural** - Menggunakan fungsi dan prosedur
2. **Berorientasi Objek** - Menggunakan class dan object
3. **Generic Programming** - Menggunakan templates
4. **Fungsional** (terbatas) - Menggunakan lambda expressions

Dalam mata kuliah ini, kita akan fokus pada paradigma **prosedural** terlebih dahulu (Pertemuan 1-12), baru kemudian diperkenalkan konsep dasar **OOP** (Pertemuan 13). Pemahaman mendalam tentang OOP akan dipelajari di mata kuliah "Pemrograman Berorientasi Objek" di Semester 3.

---

### SOLVED PROBLEM 1.3 ⭐⭐

**Soal:** Jelaskan perbedaan pendekatan prosedural dan OOP dalam membuat program "Sistem Manajemen Persenjataan". Berikan contoh struktur programnya.

**Penyelesaian:**

**Pendekatan Prosedural:**
```
Program terdiri dari fungsi-fungsi terpisah:
- tambah_senjata(nama, jenis, jumlah)
- hapus_senjata(id)
- tampilkan_senjata()
- cari_senjata(nama)

Data senjata disimpan dalam array atau struktur data global
yang dapat diakses oleh semua fungsi.
```

**Pendekatan OOP:**
```
Program terdiri dari class dan objek:
- Class Senjata:
  - Atribut: id, nama, jenis, jumlah, kondisi
  - Method: tampilkan_info(), update_kondisi()
  
- Class InventoryManager:
  - Atribut: daftar_senjata
  - Method: tambah(), hapus(), cari(), laporan()

Setiap senjata adalah objek dari class Senjata.
Data dan fungsi terkait senjata terbungkus dalam class.
```

**Perbedaan Utama:**

| Aspek | Prosedural | OOP |
|-------|-----------|-----|
| Organisasi | Fungsi-fungsi terpisah | Class dan objek |
| Data | Global atau parameter | Enkapsulasi dalam objek |
| Fokus | Apa yang dilakukan (fungsi) | Siapa yang melakukan (objek) |
| Reusability | Melalui fungsi | Melalui inheritance |
| Maintenance | Sulit jika program besar | Lebih mudah, modular |

**Kesimpulan:** Untuk program sederhana, prosedural lebih simpel. Untuk sistem kompleks seperti sistem manajemen persenjataan dengan banyak entitas yang berinteraksi, OOP lebih cocok karena lebih modular dan mudah di-maintain.

---

## 1.3 PENGENALAN BAHASA C++

### 1.3.1 Sejarah C++

C++ dikembangkan oleh **Bjarne Stroustrup** di Bell Labs pada tahun 1979 sebagai ekstensi dari bahasa C. Awalnya diberi nama "C with Classes", kemudian diubah menjadi C++ pada tahun 1983.

**Timeline Perkembangan:**
- **1979**: Bjarne Stroustrup mulai mengembangkan "C with Classes"
- **1983**: Nama diubah menjadi C++
- **1985**: Rilis buku "The C++ Programming Language" edisi pertama
- **1998**: Standar C++98 (ISO/IEC 14882:1998)
- **2011**: C++11 dengan fitur modern (auto, lambda, smart pointers)
- **2014**: C++14 (perbaikan minor)
- **2017**: C++17 (structured bindings, filesystem)
- **2020**: C++20 (concepts, modules, coroutines)
- **2023**: C++23 (fitur terbaru)

**Mengapa disebut C++?**
Operator `++` dalam C/C++ berarti increment (menambah 1). Jadi C++ secara harfiah berarti "C yang ditingkatkan" atau "C versi berikutnya".

### 1.3.2 Karakteristik C++

C++ memiliki karakteristik yang membuatnya populer hingga saat ini:

1. **Multi-paradigma**: Mendukung prosedural, OOP, generic, dan fungsional
2. **Compiled Language**: Kode sumber dikompilasi menjadi machine code yang cepat
3. **Strong Type System**: Tipe data harus dideklarasikan secara eksplisit
4. **Memory Management**: Programmer punya kontrol penuh atas memori
5. **Performance**: Sangat cepat, cocok untuk aplikasi high-performance
6. **Portability**: Dapat dikompilasi di berbagai platform
7. **Backward Compatible**: Kompatibel dengan bahasa C

### 1.3.3 Mengapa Belajar C++?

**Kelebihan C++:**
- ✅ Performa sangat tinggi (mendekati assembly)
- ✅ Kontrol penuh atas hardware dan memori
- ✅ Banyak digunakan di industri (game, sistem embedded, OS)
- ✅ Basis untuk memahami bahasa lain
- ✅ Komunitas besar dan mature
- ✅ Library yang sangat lengkap (STL, Boost, dll)

**Tantangan C++:**
- ⚠️ Kurva belajar yang curam
- ⚠️ Syntax yang kompleks
- ⚠️ Manual memory management (risiko memory leak)
- ⚠️ Compile time yang lama untuk proyek besar

**Aplikasi C++ di Dunia Nyata:**
- **Game Development**: Unreal Engine, CryEngine
- **Operating Systems**: Windows, Linux, macOS
- **Browsers**: Chrome, Firefox
- **Database**: MySQL, MongoDB
- **Embedded Systems**: Perangkat IoT, sistem kontrol industri
- **Defense Systems**: Sistem radar, command-and-control, simulasi militer
- **Finance**: High-frequency trading systems
- **Graphics**: Adobe Photoshop, AutoCAD

### 1.3.4 C++ di Konteks Pertahanan Indonesia

Di lingkungan pertahanan, C++ digunakan untuk:

1. **Sistem Komando dan Kontrol (C2)**: Sistem yang membutuhkan real-time processing dan high reliability
2. **Simulasi Militer**: Program simulasi taktik dan strategi
3. **Embedded Systems**: Software untuk perangkat militer (radar, komunikasi, navigasi)
4. **Sistem Informasi Pertahanan**: Database dan aplikasi manajemen data personel/alutsista
5. **Image Processing**: Analisis citra satelit dan drone

---

### SOLVED PROBLEM 1.4 ⭐

**Soal:** Sebutkan 3 alasan mengapa C++ cocok untuk pengembangan sistem pertahanan.

**Penyelesaian:**

**Alasan 1: Performance dan Efisiensi**
Sistem pertahanan membutuhkan real-time processing dengan latency minimal. C++ menghasilkan machine code yang sangat cepat, cocok untuk sistem radar yang harus memproses ribuan objek per detik, atau sistem command-and-control yang harus merespons dalam hitungan milidetik.

**Alasan 2: Kontrol Hardware Langsung**
C++ memberikan akses low-level ke hardware melalui pointer dan memory management manual. Ini penting untuk sistem embedded di perangkat militer seperti missile guidance systems, drone controllers, atau sistem komunikasi taktis yang harus berinteraksi langsung dengan sensor dan aktuator.

**Alasan 3: Reliability dan Portability**
C++ adalah bahasa mature dengan compiler yang tersedia di hampir semua platform (Windows, Linux, embedded RTOS). Sistem pertahanan harus reliable dan dapat berjalan di berbagai hardware. C++ juga memiliki strong type system yang membantu mencegah bugs di compile-time.

---

## 1.4 STRUKTUR DASAR PROGRAM C++

### 1.4.1 Program Hello World

Mari kita mulai dengan program C++ paling sederhana:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

*Listing 1.1: Program Hello World pertama*

Mari kita bedah baris per baris:

**Baris 1: `#include <iostream>`**
- Ini adalah **preprocessor directive** yang memberitahu compiler untuk menyertakan library `iostream`
- `iostream` singkatan dari "input-output stream", berisi fungsi untuk input/output
- `#include` bukan statement C++, tapi instruksi ke preprocessor yang dijalankan sebelum kompilasi
- Harus ditulis di awal program, sebelum kode lainnya
- Tanda `<>` menunjukkan ini adalah standard library

**Baris 2: `using namespace std;`**
- Memberitahu compiler bahwa kita menggunakan namespace `std` (standard)
- Tanpa ini, kita harus menulis `std::cout` dan `std::endl`
- Mempermudah penulisan, tapi bisa menyebabkan konflik nama di program besar
- Alternatif: tidak pakai `using namespace std;` dan tulis `std::` setiap kali

**Baris 4: `int main() {`**
- Ini adalah **fungsi utama** program
- Setiap program C++ HARUS punya fungsi `main()`
- Eksekusi program dimulai dari `main()`
- `int` berarti fungsi ini mengembalikan integer
- `()` berarti fungsi ini tidak menerima parameter (untuk saat ini)
- `{` menandai awal blok kode fungsi

**Baris 5: `cout << "Hello, World!" << endl;`**
- `cout` adalah objek untuk output ke layar (console output)
- `<<` adalah operator insertion (mengirim data ke cout)
- `"Hello, World!"` adalah string literal yang akan ditampilkan
- `endl` adalah end-line (pindah baris baru)
- `;` menandai akhir statement (wajib!)

**Baris 6: `return 0;`**
- Mengembalikan nilai 0 ke sistem operasi
- Konvensi: 0 = program berhasil, non-zero = ada error
- Wajib ada di fungsi `main()` karena tipe returnnya `int`

**Baris 7: `}`**
- Menutup blok kode fungsi `main()`

![Anatomi Program C++](images/p01-04-cpp-program-anatomy.png)

*Gambar 1.4: Anatomi program C++ sederhana*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Annotated anatomy of a C++ Hello World program with arrows pointing to different parts
STYLE: Clean flat vector illustration, educational diagram, code documentation style
LAYOUT: Code block on left (60%), annotations with arrows on right (40%)
COLORS: 
- Code background: #1e293b (dark slate)
- Code text: #e2e8f0 (light)
- Keywords: #8b5cf6 (purple)
- Strings: #10b981 (green)
- Comments: #6b7280 (gray)
- Arrows: #f59e0b (orange)
- Annotation boxes: #ffffff (white)
ELEMENTS:
1. Code block showing Hello World program with syntax highlighting
2. Arrow 1: pointing to "#include" → annotation "Preprocessor directive"
3. Arrow 2: pointing to "using namespace std" → annotation "Namespace"
4. Arrow 3: pointing to "int main()" → annotation "Fungsi utama"
5. Arrow 4: pointing to "cout << ..." → annotation "Output statement"
6. Arrow 5: pointing to "return 0" → annotation "Return value"
7. Arrow 6: pointing to braces {} → annotation "Blok kode"
LABELS: All text in Bahasa Indonesia
SIZE: 900x600 pixels
FORMAT: PNG, white background
NEGATIVE: No gradients, no complex shadows
```

### 1.4.2 Komentar dalam C++

Komentar adalah teks dalam kode yang diabaikan oleh compiler. Komentar digunakan untuk:
- Menjelaskan logika program
- Dokumentasi
- Menonaktifkan sementara sebagian kode (debugging)

C++ mendukung 2 jenis komentar:

```cpp
// Ini adalah komentar single-line
// Digunakan untuk komentar pendek, 1 baris

/* 
   Ini adalah komentar multi-line
   Bisa mencakup beberapa baris
   Cocok untuk dokumentasi panjang
*/

#include <iostream>
using namespace std;

int main() {
    // Menampilkan pesan selamat datang
    cout << "Selamat datang di Program Pertama!" << endl;
    
    /* 
       Baris berikut akan menampilkan nama program
       Format: [NAMA_PROGRAM] versi X.X
    */
    cout << "Program: Hello World v1.0" << endl;
    
    return 0; // Mengembalikan 0 (sukses)
}
```

*Listing 1.2: Penggunaan komentar dalam C++*

**Best Practices Komentar:**
- ✅ Jelaskan WHY (mengapa), bukan WHAT (apa)
- ✅ Update komentar jika kode berubah
- ✅ Gunakan komentar untuk bagian yang kompleks
- ❌ Jangan menulis komentar yang obvious
- ❌ Jangan menulis komentar terlalu banyak

**Contoh Komentar Buruk:**
```cpp
int x = 5; // Set x menjadi 5
```

**Contoh Komentar Baik:**
```cpp
int max_soldiers = 50; // Batas maksimal prajurit per regu sesuai SOP TNI AD
```

---

### SOLVED PROBLEM 1.5 ⭐

**Soal:** Apa yang salah dengan program berikut? Perbaiki dan jelaskan.

```cpp
include <iostream>
using namespace std

int main() {
    cout << "Halo Dunia" << endl
    return 0;
}
```

**Penyelesaian:**

Ada **3 kesalahan**:

**Kesalahan 1:** `include <iostream>` → harus `#include <iostream>`
- Preprocessor directive harus diawali dengan `#`

**Kesalahan 2:** `using namespace std` → harus `using namespace std;`
- Setiap statement C++ harus diakhiri dengan semicolon `;`

**Kesalahan 3:** `cout << "Halo Dunia" << endl` → harus `cout << "Halo Dunia" << endl;`
- Statement output juga harus diakhiri dengan semicolon

**Program yang benar:**
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Halo Dunia" << endl;
    return 0;
}
```

**Catatan:** Jika program ini dikompilasi dengan kesalahan, compiler akan memberikan error messages yang menunjukkan baris-baris yang bermasalah.

---

### SOLVED PROBLEM 1.6 ⭐⭐

**Soal:** Modifikasi program Hello World untuk menampilkan output berikut:
```
=============================
  SISTEM INFORMASI PRAJURIT
=============================
Versi: 1.0
Developer: Taruna DataForce
=============================
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "=============================" << endl;
    cout << "  SISTEM INFORMASI PRAJURIT" << endl;
    cout << "=============================" << endl;
    cout << "Versi: 1.0" << endl;
    cout << "Developer: Taruna DataForce" << endl;
    cout << "=============================" << endl;
    
    return 0;
}
```

*Listing 1.3: Program dengan multiple output statements*

**Penjelasan:**
- Setiap `cout` statement menghasilkan 1 baris output
- `endl` memindahkan kursor ke baris baru
- Tanda `=` ditulis sebagai string literal di dalam double quotes
- Multiple statements dieksekusi secara berurutan dari atas ke bawah

**Alternatif (tanpa endl):**
```cpp
cout << "=============================\n";
cout << "  SISTEM INFORMASI PRAJURIT\n";
cout << "=============================\n";
cout << "Versi: 1.0\n";
cout << "Developer: Taruna DataForce\n";
cout << "=============================\n";
```

Keterangan: `\n` adalah **escape sequence** untuk newline (sama dengan `endl`).

---

## 1.5 PROSES KOMPILASI DAN EKSEKUSI

### 1.5.1 Dari Source Code ke Executable

Program C++ tidak langsung dijalankan. Ia harus melewati beberapa tahap:

![Proses Kompilasi C++](images/p01-05-compilation-process.png)

*Gambar 1.5: Tahapan kompilasi program C++*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: C++ compilation process flowchart showing 4 stages with file types
STYLE: Clean flat vector illustration, technical diagram, process flow
LAYOUT: Horizontal flow from left to right with arrows
COLORS: 
- Stage 1 (Source): #3b82f6 (blue)
- Stage 2 (Preprocessor): #10b981 (green)
- Stage 3 (Compiler): #f59e0b (orange)
- Stage 4 (Linker): #ef4444 (red)
- Final (Executable): #8b5cf6 (purple)
- Arrows: #6b7280 (gray)
- Background: #ffffff (white)
ELEMENTS:
1. Box 1: "Source Code" + file icon ".cpp" (blue)
2. Arrow → "Preprocessor"
3. Box 2: "Expanded Source" + file icon ".i" (green)
4. Arrow → "Compiler"
5. Box 3: "Object Code" + file icon ".o" (orange)
6. Arrow → "Linker" + library files joining
7. Box 4: "Executable" + file icon ".exe" (purple)
8. Each box has small description in Indonesian
LABELS: All text in Bahasa Indonesia
SIZE: 1000x400 pixels
FORMAT: PNG, white background
NEGATIVE: No gradients, no 3D effects
```

**Tahap 1: Preprocessing**
- Preprocessor memproses directives yang diawali `#`
- `#include` → menyalin isi file header ke source code
- `#define` → mengganti macro dengan nilainya
- Hasilnya: file `.i` (expanded source code)

**Tahap 2: Compilation**
- Compiler mengubah source code menjadi assembly code
- Melakukan syntax checking dan type checking
- Hasilnya: file `.s` (assembly code), kemudian `.o` atau `.obj` (object code)

**Tahap 3: Linking**
- Linker menggabungkan object files dengan library files
- Menyelesaikan external references (fungsi dari library)
- Hasilnya: file executable (`.exe` di Windows, tidak ada ekstensi di Linux)

**Tahap 4: Execution**
- Executable dijalankan oleh sistem operasi
- Program dimuat ke memory dan dieksekusi

---

![Dito Belajar Kompilasi](images/p01-06-comic-kompilasi.png)

*Gambar 1.6: Dito bingung dengan error kompilasi, Ira menjelaskan proses compilation*

**[GEMINI COMIC PROMPT]**
```
SUBJECT: Webtoon comic panel — Dito confused looking at compiler errors on screen, Ira explaining the compilation process with diagram
STYLE: Clean anime-inspired webtoon art, educational comic, DataForce Academy computer lab setting
CHARACTERS: 
- DITO: Indonesian male, 18 years old, 175cm, athletic build. Hair: jet black, short military cut (3cm), neat side part on LEFT. Face: oval shape, strong jawline, thick straight eyebrows, dark brown eyes, SMALL SCAR on RIGHT CHEEK near ear. Uniform: white short-sleeve dress shirt tucked in, red/maroon epaulettes with gold trim, black leather belt with gold buckle, olive/khaki trousers, DataForce Academy badge (Garuda emblem) on left chest, short NAME TAG "DITO" on right chest. Expression: confused, eyebrows furrowed, mouth slightly open, hand scratching head near right ear.
- IRA: Indonesian female, 18 years old, 165cm, athletic build. Hair: black, HIGH PONYTAIL with RED hair tie, bangs swept to RIGHT. Face: heart-shaped, sharp intelligent eyes, thin eyebrows, beauty mark below RIGHT eye. Wearing: RED-FRAMED rectangular tactical glasses. Uniform: white short-sleeve dress shirt tucked in, red/maroon epaulettes with gold trim, black belt with gold buckle, olive trousers, DataForce Academy badge on left chest, NAME TAG "IRA" on right chest. Holding: BLACK TABLET in LEFT hand showing simple flowchart. Expression: explaining patiently, slight knowing smile, one finger pointing to tablet.
SCENE: Computer lab with rows of desks. Dito sitting at computer desk with Code::Blocks open on screen showing red error messages. Ira standing beside him, leaning slightly forward, showing him diagram on her tablet.
LAYOUT: Panel divided - left side shows Dito's confused face and error-filled screen, right side shows Ira explaining with tablet showing: "Source (.cpp) → Compiler → Object (.o) → Linker → .exe"
DIALOGUE (in speech bubbles): 
- Dito (confused): "Kok error terus, Ira? Aku udah tulis sesuai contoh!"
- Ira (patient): "Tenang, Dito. Lihat baris 7—kamu lupa titik koma. Compiler check syntax dulu sebelum jadi executable."
BACKGROUND: Computer lab, other computers visible in background, whiteboard with "Pertemuan 1" written on it
MOOD: Educational, supportive, relatable student struggle moment
SIZE: 800x600 pixels
FORMAT: PNG, clean background
NEGATIVE: No 3D effects, no photorealistic elements, no flags on uniforms
```

**Penjelasan Scene:**
Panel komik ini menggambarkan situasi yang sangat relatable bagi mahasiswa baru yang belajar programming. Dito mengalami kesulitan dengan error kompilasi—sesuatu yang dialami hampir setiap programmer pemula. Ira, dengan karakternya yang metodis dan sabar, menjelaskan bahwa compiler melakukan syntax checking di tahap compilation sebelum menghasilkan executable. Scene ini mengajarkan bahwa error itu normal dan merupakan bagian dari proses belajar.

---

### 1.5.2 Compiler dan IDE

**Compiler** adalah program yang mengubah source code menjadi machine code.

Compiler C++ yang populer:
- **GCC (GNU Compiler Collection)** - Open source, tersedia di Linux/Windows/macOS
- **Clang** - Modern, error messages yang lebih baik
- **MSVC (Microsoft Visual C++)** - Untuk Windows
- **MinGW** - Port GCC untuk Windows (yang kita gunakan)

**IDE (Integrated Development Environment)** adalah aplikasi yang menggabungkan:
- **Text Editor** - Untuk menulis kode
- **Compiler** - Untuk compile kode
- **Debugger** - Untuk mencari bug
- **Build Tools** - Untuk manage proyek

IDE C++ yang populer:
- **Code::Blocks** ← (kita gunakan ini)
- **Visual Studio**
- **CLion**
- **Dev-C++**
- **Eclipse CDT**

**Mengapa Code::Blocks?**
- ✅ Open source dan gratis
- ✅ Ringan dan cepat
- ✅ Cross-platform (Windows, Linux, macOS)
- ✅ Sudah include compiler MinGW
- ✅ User-friendly untuk pemula
- ✅ Debugger terintegrasi

### 1.5.3 Error Messages dan Debugging

Ketika compile program, kita bisa mendapat 3 jenis masalah:

**1. Compile-time Errors (Syntax Errors)**
Terjadi saat kompilasi karena syntax yang salah.

Contoh:
```cpp
cout << "Hello"  // Error: missing semicolon
```

Error message:
```
error: expected ';' before 'return'
```

**2. Linker Errors**
Terjadi saat linking karena fungsi/variable tidak ditemukan.

Contoh:
```cpp
int main() {
    someFunction(); // Error: someFunction() not defined
    return 0;
}
```

Error message:
```
undefined reference to `someFunction()'
```

**3. Runtime Errors (Logical Errors)**
Program berhasil dikompilasi tapi menghasilkan output salah atau crash saat dijalankan.

Contoh:
```cpp
int x = 10;
int y = 0;
int z = x / y; // Error: division by zero (runtime)
```

**Tips Debugging untuk Pemula:**
1. **Baca error message dengan teliti** - Compiler memberitahu line number dan jenis error
2. **Cek semicolon** - 80% error pemula karena lupa semicolon
3. **Cek kurung** - Pastikan setiap `{` punya pasangan `}`
4. **Cek spelling** - `cout` vs `cuot`, `endl` vs `end1`
5. **Compile sering** - Jangan menunggu program selesai, compile setiap beberapa baris

---

### SOLVED PROBLEM 1.7 ⭐

**Soal:** Jelaskan perbedaan antara compiler error dan runtime error. Berikan contoh masing-masing.

**Penyelesaian:**

**Compiler Error (Compile-time Error):**
- Terjadi saat proses kompilasi
- Disebabkan oleh syntax yang salah
- Program tidak bisa dikompilasi menjadi executable
- Compiler memberikan error message yang jelas
- Harus diperbaiki sebelum program bisa dijalankan

Contoh:
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello"  // COMPILER ERROR: missing semicolon
    return 0;
}
```

Error message: `error: expected ';' before 'return'`

**Runtime Error (Logical Error):**
- Terjadi saat program dijalankan
- Program berhasil dikompilasi, tapi ada kesalahan logika
- Bisa menyebabkan crash atau hasil yang salah
- Tidak ada error message dari compiler
- Lebih sulit dideteksi karena tidak ditangkap compiler

Contoh:
```cpp
#include <iostream>
using namespace std;

int main() {
    int prajurit = 100;
    int regu = 0;
    int prajurit_per_regu = prajurit / regu; // RUNTIME ERROR: division by zero
    
    cout << "Prajurit per regu: " << prajurit_per_regu << endl;
    return 0;
}
```

Program ini berhasil dikompilasi, tapi saat dijalankan akan crash karena division by zero.

**Kesimpulan:**
- **Compiler error** → mudah dideteksi, harus diperbaiki sebelum program jalan
- **Runtime error** → sulit dideteksi, perlu testing dan debugging mendalam

---

### SOLVED PROBLEM 1.8 ⭐⭐

**Soal:** Program berikut menghasilkan error. Identifikasi semua error dan perbaiki programnya.

```cpp
#include iostream
using namespace std

int main() 
{
    cout << Selamat datang di program C++ << endl;
    cout << "Mari belajar bersama" << end;
    return 0
}
```

**Penyelesaian:**

**Error yang ditemukan:**

**Error 1 (Baris 1):** `#include iostream` → harus `#include <iostream>`
- Preprocessor directive harus pakai `#` dan library header harus dalam `< >`

**Error 2 (Baris 2):** `using namespace std` → harus `using namespace std;`
- Statement harus diakhiri semicolon

**Error 3 (Baris 6):** `Selamat datang di program C++` → harus `"Selamat datang di program C++"`
- String literal harus diapit double quotes

**Error 4 (Baris 7):** `end` → harus `endl`
- Typo, harusnya `endl` (end-line)

**Error 5 (Baris 8):** `return 0` → harus `return 0;`
- Statement harus diakhiri semicolon

**Program yang benar:**
```cpp
#include <iostream>
using namespace std;

int main() 
{
    cout << "Selamat datang di program C++" << endl;
    cout << "Mari belajar bersama" << endl;
    return 0;
}
```

---

## 1.6 INSTALASI DAN KONFIGURASI CODE::BLOCKS

### 1.6.1 Download dan Instalasi

**Langkah 1: Download Code::Blocks**
1. Buka website: https://www.codeblocks.org/downloads/
2. Pilih versi **"codeblocks-XX.XX-mingw-setup.exe"** (yang include MinGW compiler)
3. Download file installer (ukuran ±100 MB)

**Langkah 2: Instalasi**
1. Jalankan file installer
2. Klik "Next" → "I Agree" → "Next"
3. Pilih "Full installation" (termasuk compiler)
4. Pilih lokasi instalasi (default: `C:\Program Files\CodeBlocks`)
5. Klik "Install" dan tunggu hingga selesai
6. Klik "Finish"

**Langkah 3: Konfigurasi Pertama Kali**
1. Jalankan Code::Blocks
2. Jika muncul dialog "Compiler auto-detection", klik "OK"
3. Code::Blocks akan mendeteksi compiler MinGW yang sudah terinstall
4. Jika berhasil, akan muncul notifikasi "GNU GCC Compiler detected"

---

![Bram Instalasi Code::Blocks](images/p01-07-comic-instalasi.png)

*Gambar 1.7: Bram kesulitan instalasi Code::Blocks, Letda Saepul membantu*

**[GEMINI COMIC PROMPT]**
```
SUBJECT: Webtoon comic panel — Bram struggling with Code::Blocks installation on laptop, Letda Saepul helping him step-by-step
STYLE: Clean anime-inspired webtoon art, educational comic, DataForce Academy computer lab setting
CHARACTERS: 
- BRAM: Indonesian male, 19 years old, 185cm - TALLEST and LARGEST build (tall, broad, stocky). Hair: black, slightly messy/spiky, medium length (5-6cm). Face: round and friendly, chubby cheeks, small warm eyes, wide nose, TAN SKIN darker than other characters. Uniform: white short-sleeve dress shirt (slightly tight on large frame), red/maroon epaulettes with gold trim, black belt, olive trousers, DataForce Academy badge on left chest, NAME TAG "BRAM" on right chest. Accessory: GREEN BANDANA on RIGHT wrist. Expression: confused and slightly stressed, sweating on forehead, eyes squinting at screen.
- LETDA SAEPUL: Indonesian male, 27 years old, 173cm, fit athletic build. Face: youthful but professional, oval, warm brown eyes, SMALL MOLE on RIGHT side of nose, easy smile. Hair: black, short military cut with SLIGHT FADE on sides, clean-shaven (NO beard). Uniform (INSTRUCTOR): white dress shirt, OFFICER epaulettes with Letnan Dua rank insignia, DataForce Academy badge, black belt, olive trousers. Accessory: BLACK SMARTWATCH on left wrist. Expression: patient and encouraging, slight smile, pointing at screen with right hand.
SCENE: Computer lab. Bram sitting at desk with laptop open showing Code::Blocks installer window. Letda Saepul standing beside him, leaning down to point at screen, left hand on Bram's shoulder in supportive gesture.
LAYOUT: Two-panel horizontal split. Left panel: Bram's stressed face close-up with sweat drop. Right panel: Letda Saepul pointing at screen showing installer dialog "Choose Components: Full Installation ✓"
DIALOGUE (in speech bubbles): 
- Bram (stressed): "Pak Letda, ini kok ada pilihan banyak? Yang mana yang harus dipilih?"
- Letda Saepul (calm): "Tenang, Bram. Pilih 'Full Installation' biar compiler MinGW langsung terinstall. Gampang kan?"
BACKGROUND: Computer lab, other students working in background (blurred), window showing DataForce Academy building outside
MOOD: Supportive mentorship, instructional, relatable tech setup struggle
SIZE: 800x600 pixels
FORMAT: PNG, clean background
NEGATIVE: No 3D effects, no photorealistic elements, no flags on uniforms
```

**Penjelasan Scene:**
Panel komik ini menampilkan Bram—karakter yang merepresentasikan mahasiswa yang kesulitan dengan aspek teknis—mengalami kebingungan saat instalasi IDE. Letda Saepul, sebagai instruktur muda yang relatable, memberikan bantuan dengan sabar dan jelas. Scene ini mengajarkan bahwa tidak apa-apa untuk bertanya dan meminta bantuan saat menghadapi kesulitan teknis. Pilihan "Full Installation" memastikan compiler MinGW terinstall otomatis.

---

![Tampilan Code::Blocks](images/p01-08-codeblocks-interface.png)

*Gambar 1.8: Interface utama Code::Blocks IDE*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Screenshot mockup of Code::Blocks IDE interface with labeled sections
STYLE: Clean interface mockup, software screenshot style, educational annotation
LAYOUT: Full IDE window with numbered annotations
COLORS: 
- IDE background: #f8f9fa (light gray)
- Menu bar: #e9ecef (gray)
- Editor: #ffffff (white)
- Console: #1e293b (dark)
- Annotations: #f59e0b (orange boxes with numbers)
ELEMENTS:
1. Top: Menu bar (File, Edit, View, Search, Build, Debug, Tools)
2. Left: Project tree panel showing "Hello World" project
3. Center: Code editor with sample C++ code
4. Bottom: Build log and console output panel
5. Right: Management panel (optional, can be collapsed)
6. Annotations pointing to:
   - "Menu Bar" → 1
   - "Toolbar" → 2
   - "Project Tree" → 3
   - "Code Editor" → 4
   - "Build Log" → 5
   - "Console Output" → 6
LABELS: All annotations in Bahasa Indonesia
SIZE: 1000x700 pixels
FORMAT: PNG, white background
NEGATIVE: No real screenshots, use mockup illustration style
```

### 1.6.2 Membuat Project Pertama

**Langkah 1: Buat Project Baru**
1. Klik menu `File` → `New` → `Project...`
2. Pilih `Console Application` → `Go`
3. Pilih bahasa `C++` → `Next`
4. Beri nama project: `HelloWorld`
5. Pilih folder untuk menyimpan project
6. Pilih compiler: `GNU GCC Compiler`
7. Klik `Finish`

**Langkah 2: Struktur Project**
Code::Blocks akan membuat struktur folder:
```
HelloWorld/
├── HelloWorld.cbp        (project file)
├── main.cpp              (source code)
├── bin/                  (executable files)
│   └── Debug/
│       └── HelloWorld.exe
└── obj/                  (object files)
    └── Debug/
        └── main.o
```

**Langkah 3: Menulis Kode**
File `main.cpp` sudah terisi template:
```cpp
#include <iostream>

using namespace std;

int main()
{
    cout << "Hello world!" << endl;
    return 0;
}
```

### 1.6.3 Compile dan Run

**Cara 1: Menggunakan Tombol**
- `Build` (Ctrl + F9) → Hanya compile, tidak run
- `Run` (Ctrl + F10) → Run program yang sudah dikompilasi
- `Build and Run` (F9) → Compile + Run sekaligus ← (PALING SERING DIPAKAI)

**Cara 2: Menggunakan Menu**
- Menu `Build` → `Build and Run`

**Output:**
Jika berhasil, akan muncul console window:
```
Hello world!

Process returned 0 (0x0)   execution time : 0.001 s
Press any key to continue.
```

**Keterangan:**
- `Hello world!` → output dari program
- `Process returned 0` → program selesai dengan sukses (return 0)
- `execution time` → waktu eksekusi program
- `Press any key to continue` → tunggu user sebelum close console

### 1.6.4 Debugger Dasar

**Debugger** adalah tool untuk mencari dan memperbaiki bug dalam program.

**Fitur debugger dasar:**
1. **Breakpoint** - Menandai baris untuk pause eksekusi
2. **Step Over** - Jalankan baris berikutnya
3. **Step Into** - Masuk ke dalam fungsi
4. **Watch Variables** - Monitor nilai variabel

**Cara menggunakan:**
1. Klik di sebelah kiri nomor baris untuk set breakpoint (muncul lingkaran merah)
2. Klik `Debug` → `Start/Continue` (F8)
3. Program akan pause di breakpoint
4. Gunakan `Next Line` (F7) untuk step over
5. Lihat nilai variabel di panel "Watches"

![Debugging dengan Breakpoint](images/p01-07-debugging-breakpoint.png)

*Gambar 1.7: Menggunakan breakpoint untuk debugging*

**[GEMINI IMAGE PROMPT]**
```
SUBJECT: Code::Blocks debugger interface showing breakpoint and variable watch
STYLE: Clean interface mockup, debugging screenshot style
LAYOUT: Split view - code editor (60%) and watches panel (40%)
COLORS: 
- Editor background: #ffffff (white)
- Breakpoint: #ef4444 (red circle)
- Current line: #fef3c7 (yellow highlight)
- Watch panel: #f8f9fa (light gray)
- Variable names: #2563eb (blue)
- Variable values: #10b981 (green)
ELEMENTS:
1. Code editor showing simple C++ program with breakpoint
2. Red circle on line 6 (breakpoint marker)
3. Yellow highlight on line 7 (current execution line)
4. Right panel: "Watches" showing variables:
   - x: 10
   - y: 20
   - sum: 30
5. Debug toolbar at top with step buttons
6. Annotations pointing to breakpoint and current line
LABELS: All text in Bahasa Indonesia
SIZE: 900x500 pixels
FORMAT: PNG, white background
NEGATIVE: No complex UI, keep it simple and clear
```

**Tips Debugging:**
- Set breakpoint di baris yang dicurigai bermasalah
- Watch variabel untuk melihat perubahan nilainya
- Step over line by line untuk memahami alur eksekusi
- Jika program crash, lihat call stack untuk tahu di mana errornya

---

### SOLVED PROBLEM 1.9 ⭐

**Soal:** Jelaskan perbedaan antara "Build", "Run", dan "Build and Run" di Code::Blocks.

**Penyelesaian:**

**Build (Ctrl + F9):**
- Hanya melakukan kompilasi source code
- Menghasilkan file executable (.exe)
- TIDAK menjalankan program
- Digunakan untuk:
  - Cek apakah ada compile error
  - Membuat executable tanpa langsung run
  - Build project besar yang lama (tidak perlu run berkali-kali)

**Run (Ctrl + F10):**
- Hanya menjalankan executable yang sudah ada
- TIDAK melakukan kompilasi ulang
- Digunakan untuk:
  - Run program yang sudah pernah di-build
  - Testing cepat tanpa compile ulang (jika kode tidak berubah)

**Build and Run (F9):**
- Melakukan Build KEMUDIAN Run
- Shortcut paling sering dipakai
- Digunakan untuk:
  - Development normal (edit kode → test → edit lagi)
  - Memastikan perubahan kode ter-compile sebelum run

**Analogi Militer:**
- **Build** = Menyiapkan senjata dan amunisi
- **Run** = Menembak dengan senjata yang sudah disiapkan
- **Build and Run** = Siapkan senjata DAN langsung tembak

**Flowchart Keputusan:**
```
Apakah kode berubah?
├─ Ya → Pakai "Build and Run" (F9)
└─ Tidak
   ├─ Ingin compile saja → Pakai "Build" (Ctrl+F9)
   └─ Ingin run saja → Pakai "Run" (Ctrl+F10)
```

**Best Practice:** Gunakan **F9** (Build and Run) untuk development sehari-hari. Ini memastikan program selalu ter-compile dengan perubahan terbaru sebelum dijalankan.

---

### SOLVED PROBLEM 1.10 ⭐⭐

**Soal:** Buatlah project Code::Blocks baru dengan nama "DataPrajurit" yang menampilkan:
```
=================================
   SISTEM DATA PRAJURIT TNI AD
=================================
Nama    : Serka Budi Santoso
NRP     : 31200045
Satuan  : Yonif 123 Raider
Pangkat : Sersan Kepala
=================================
```

Jelaskan langkah-langkahnya dan tuliskan kode lengkapnya.

**Penyelesaian:**

**Langkah-langkah:**

**1. Buat Project Baru**
- File → New → Project
- Pilih "Console Application" → Go
- Pilih "C++" → Next
- Project title: `DataPrajurit`
- Folder: Pilih lokasi (misalnya `D:\Kuliah\DDP\`)
- Compiler: GNU GCC Compiler
- Finish

**2. Edit main.cpp**
Ganti isi file `main.cpp` dengan kode berikut:

```cpp
/*
 * Program: Sistem Data Prajurit TNI AD
 * Deskripsi: Menampilkan informasi data prajurit
 * Author: Taruna DataForce Academy
 * Tanggal: [Tanggal sekarang]
 */

#include <iostream>
using namespace std;

int main()
{
    // Header sistem
    cout << "=================================" << endl;
    cout << "   SISTEM DATA PRAJURIT TNI AD" << endl;
    cout << "=================================" << endl;
    
    // Data prajurit
    cout << "Nama    : Serka Budi Santoso" << endl;
    cout << "NRP     : 31200045" << endl;
    cout << "Satuan  : Yonif 123 Raider" << endl;
    cout << "Pangkat : Sersan Kepala" << endl;
    
    // Footer
    cout << "=================================" << endl;
    
    return 0;
}
```

*Listing 1.4: Program sistem data prajurit*

**3. Build and Run**
- Tekan F9 atau klik ikon "Build and Run"
- Console window akan muncul dengan output yang diminta

**Penjelasan Kode:**

**Baris 1-6:** Komentar dokumentasi
- Memberikan informasi tentang program
- Good practice untuk setiap program

**Baris 8:** `#include <iostream>`
- Menyertakan library untuk input/output

**Baris 9:** `using namespace std;`
- Memudahkan penggunaan cout dan endl

**Baris 11:** `int main()`
- Fungsi utama program

**Baris 13-15:** Menampilkan header
- 3 statement cout untuk 3 baris header

**Baris 17-21:** Menampilkan data prajurit
- Menggunakan spasi untuk alignment
- Format: `Label    : Nilai`

**Baris 23-24:** Menampilkan footer dan return

**Tips:**
- Untuk alignment yang rapi, gunakan spasi yang konsisten
- Setiap `cout` statement menghasilkan 1 baris output
- `endl` penting untuk pindah baris baru

---

## 1.7 PROGRAM C++ SEDERHANA: VARIASI OUTPUT

### 1.7.1 Variasi Penggunaan cout

Operator `<<` dapat digunakan beberapa kali dalam satu statement:

```cpp
#include <iostream>
using namespace std;

int main() {
    // Cara 1: Multiple cout statements
    cout << "Baris 1" << endl;
    cout << "Baris 2" << endl;
    cout << "Baris 3" << endl;
    
    // Cara 2: Chain dalam satu statement
    cout << "Baris 1" << endl << "Baris 2" << endl << "Baris 3" << endl;
    
    // Cara 3: Multiple << dalam satu cout
    cout << "Nama: " << "Dito" << endl;
    cout << "Usia: " << 18 << " tahun" << endl;
    
    return 0;
}
```

*Listing 1.5: Variasi penggunaan cout*

### 1.7.2 Escape Sequences

**Escape sequence** adalah karakter khusus yang diawali backslash `\`.

| Escape Sequence | Arti | Contoh |
|----------------|------|--------|
| `\n` | New line (baris baru) | `cout << "Baris 1\nBaris 2";` |
| `\t` | Tab (8 spasi) | `cout << "Nama\tNRP";` |
| `\\` | Backslash | `cout << "C:\\Users\\";` |
| `\"` | Double quote | `cout << "Dia berkata \"Halo\"";` |
| `\'` | Single quote | `cout << "It\'s okay";` |
| `\r` | Carriage return | `cout << "Loading\r100%";` |
| `\b` | Backspace | `cout << "Testt\b";` |
| `\a` | Alert (beep) | `cout << "\a";` |

Contoh penggunaan:

```cpp
#include <iostream>
using namespace std;

int main() {
    // Menggunakan \n untuk newline
    cout << "Baris 1\nBaris 2\nBaris 3\n";
    
    // Menggunakan \t untuk tab
    cout << "Nama\tNRP\tSatuan\n";
    cout << "Dito\t123\tAlfa\n";
    cout << "Ira\t456\tBravo\n";
    
    // Menggunakan \" untuk quotes
    cout << "Letda Saepul berkata: \"Selamat pagi, Kadet!\"\n";
    
    // Menggunakan \\ untuk backslash
    cout << "File location: C:\\Program Files\\CodeBlocks\n";
    
    return 0;
}
```

*Listing 1.6: Penggunaan escape sequences*

**Output:**
```
Baris 1
Baris 2
Baris 3
Nama    NRP     Satuan
Dito    123     Alfa
Ira     456     Bravo
Letda Saepul berkata: "Selamat pagi, Kadet!"
File location: C:\Program Files\CodeBlocks
```

---

### SOLVED PROBLEM 1.11 ⭐

**Soal:** Buatlah program yang menampilkan tabel berikut menggunakan escape sequences:
```
NO      NAMA            PANGKAT
1       Dito            Kadet
2       Ira             Kadet
3       Bram            Kadet
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "NO\tNAMA\t\tPANGKAT\n";
    cout << "1\tDito\t\tKadet\n";
    cout << "2\tIra\t\tKadet\n";
    cout << "3\tBram\t\tKadet\n";
    
    return 0;
}
```

*Listing 1.7: Program tabel menggunakan \t*

**Penjelasan:**
- `\t` membuat tab (sekitar 8 spasi)
- `\n` membuat newline (sama dengan `endl`)
- Untuk nama yang pendek (seperti "Ira"), kita pakai `\t\t` (double tab) agar tetap rapi
- Lebih efisien daripada menggunakan banyak `cout` statement

**Alternatif tanpa escape sequences:**
```cpp
cout << "NO" << "\t" << "NAMA" << "\t\t" << "PANGKAT" << endl;
cout << "1" << "\t" << "Dito" << "\t\t" << "Kadet" << endl;
cout << "2" << "\t" << "Ira" << "\t\t" << "Kadet" << endl;
cout << "3" << "\t" << "Bram" << "\t\t" << "Kadet" << endl;
```

Hasilnya sama, tapi lebih panjang.

---

### SOLVED PROBLEM 1.12 ⭐⭐

**Soal:** Buatlah program yang menampilkan logo ASCII sederhana untuk DataForce Academy:
```
 ____    ___ 
|  _ \  |  _|
| | | | | |_ 
| |_| | |  _|
|____/  |_|  
DataForce Academy
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << " ____    ___ " << endl;
    cout << "|  _ \\  |  _|" << endl;
    cout << "| | | | | |_ " << endl;
    cout << "| |_| | |  _|" << endl;
    cout << "|____/  |_|  " << endl;
    cout << "DataForce Academy" << endl;
    
    return 0;
}
```

*Listing 1.8: Program ASCII art logo*

**Penjelasan:**
- Karakter `\` harus ditulis `\\` karena `\` adalah escape character
- Spasi di dalam string literal dipertahankan
- Perlu teliti dalam menulis ASCII art agar alignment-nya benar
- Bisa menggunakan `\n` atau `endl`, hasilnya sama

**Tips untuk ASCII Art:**
- Gunakan text editor dengan monospace font
- Desain dulu ASCII art di notepad/text editor
- Copy-paste ke dalam string, tapi ingat escape character
- Test compile berkali-kali untuk memastikan alignment

---

### SOLVED PROBLEM 1.13 ⭐

**Soal:** Modifikasi program sebelumnya untuk menampilkan box dengan border:
```
+--------------------------------+
|   DATAFORCE MILITARY ACADEMY   |
|      "Cerdas, Berani, Jaya"    |
+--------------------------------+
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "+--------------------------------+" << endl;
    cout << "|   DATAFORCE MILITARY ACADEMY   |" << endl;
    cout << "|      \"Cerdas, Berani, Jaya\"    |" << endl;
    cout << "+--------------------------------+" << endl;
    
    return 0;
}
```

*Listing 1.9: Program box dengan border*

**Penjelasan:**
- Karakter `+`, `-`, dan `|` digunakan untuk membuat border
- Spasi digunakan untuk centering text
- `\"` digunakan untuk menampilkan double quotes di dalam string
- Perlu hitung manual jumlah karakter agar box simetris

**Perhitungan Box:**
```
Border atas/bawah: 1 (+) + 32 (-) + 1 (+) = 34 karakter
Border samping   : 1 (|) + 32 (isi) + 1 (|) = 34 karakter
Isi baris 1      : 3 spasi + 25 huruf + 4 spasi = 32
Isi baris 2      : 6 spasi + 20 huruf + 6 spasi = 32
```

---

## 1.8 KOMIK DATAFORCE ACADEMY: PERTEMUAN PERTAMA

Mari kita lihat bagaimana karakter DataForce Academy menghadapi pertemuan pertama mata kuliah DDP.

![Komik: First Day of Programming](images/p01-08-comic-first-day.png)

*Gambar 1.8: Dito, Ira, dan Bram di hari pertama kuliah DDP*

**[GEMINI COMIC PROMPT]**
```
SUBJECT: Webtoon comic panel - Three military academy cadets in classroom looking excited and nervous on first day of programming class
STYLE: Clean anime-inspired webtoon art, educational comic, DataForce Academy setting
CHARACTERS:
- DITO: Indonesian male, 18yo, 175cm, athletic. Black hair short military cut 3cm, side part on LEFT. Oval face, strong jaw, thick eyebrows, dark brown eyes, SMALL SCAR on RIGHT CHEEK near ear. White short-sleeve dress shirt tucked in, red/maroon epaulettes with gold trim, black belt with gold buckle, olive/khaki trousers. DataForce Academy badge on left chest, "DITO" name tag on right. SILVER DOG TAG visible at collar.
- IRA: Indonesian female, 18yo, 165cm, athletic. Black hair in HIGH PONYTAIL with RED hair tie, bangs swept to RIGHT. Heart-shaped face, sharp eyes, RED-FRAMED rectangular glasses, beauty mark below RIGHT eye. White dress shirt tucked in, red/maroon epaulettes, black belt, olive trousers. "IRA" name tag. BLACK TABLET in LEFT hand.
- BRAM: Indonesian male, 19yo, 185cm, LARGEST/TALLEST, broad stocky build. Black hair slightly messy/spiky. Round friendly face, chubby cheeks, TAN SKIN darker than others. White shirt slightly tight on large frame, red/maroon epaulettes, olive trousers. "BRAM" name tag. GREEN BANDANA on RIGHT wrist.
SCENE: Modern classroom at DataForce Academy. Large screen showing "DASAR-DASAR PEMROGRAMAN - Pertemuan 1". Three cadets sitting at desks with laptops.
DIALOGUE (in Indonesian):
Dito (excited): "Akhirnya! Kuliah pemrograman pertama kita!"
Ira (confident, adjusting glasses): "Sudah siap. Saya sudah baca materi duluan."
Bram (nervous, scratching head): "Aduh... coding itu sulit nggak ya?"
MOOD: Excited anticipation, first day energy, academic setting
SIZE: 800x600 pixels
FORMAT: PNG, clean background
```

![Komik: Hello World Moment](images/p01-09-comic-hello-world.png)

*Gambar 1.9: Momen pertama kali berhasil compile program Hello World*

**[GEMINI COMIC PROMPT]**
```
SUBJECT: Webtoon comic panel - Same three cadets successfully running their first Hello World program, showing excitement
STYLE: Clean anime-inspired webtoon art, educational comic, DataForce Academy setting
CHARACTERS: [Same as previous: Dito, Ira, Bram with exact same descriptions]
SCENE: Computer lab. Screen showing Code::Blocks IDE with "Hello, World!" in console output. Dito pumping fist in victory, Ira with satisfied smile, Bram with big surprised smile.
DIALOGUE (in Indonesian):
Dito (triumphant): "BERHASIL! Program pertama saya jalan!"
Ira (matter-of-fact): "Tentu saja berhasil. Syntax-nya sudah benar."
Bram (amazed, big smile): "Wah! Komputer bisa ngomong 'Hello World'! Keren!"
Letda SAEPUL (instructor, standing behind them, smiling): "Bagus! Ini langkah pertama kalian jadi programmer."
INSTRUCTOR: Indonesian male, 27yo, 173cm. Oval face, black hair short with SLIGHT FADE on sides, clean-shaven (no beard), warm brown eyes, SMALL MOLE on RIGHT side of nose, easy smile. White dress shirt, OFFICER epaulettes with Letnan Dua rank (single gold bar with star), black belt, olive trousers. BLACK SMARTWATCH on left wrist.
MOOD: Achievement, encouragement, learning success
SIZE: 800x600 pixels
FORMAT: PNG, clean background
```

![Komik: Debugging First Error](images/p01-10-comic-debugging.png)

*Gambar 1.10: Bram menghadapi error pertamanya*

**[GEMINI COMIC PROMPT]**
```
SUBJECT: Webtoon comic panel - Bram looking confused at error message, Ira helping him debug
STYLE: Clean anime-inspired webtoon art, educational comic, DataForce Academy setting
CHARACTERS: [Same Ira and Bram descriptions as before]
SCENE: Computer lab. Bram's screen showing red error text. Bram looking stressed with sweat drops. Ira leaning over pointing at screen with tablet in other hand.
DIALOGUE (in Indonesian):
Bram (stressed, reading error): "error: expected ';' before 'return'... Apa artinya ini?"
Ira (patient, pointing at screen): "Lihat baris 5. Kamu lupa semicolon setelah cout."
Bram (realization): "Oh! Titik koma! Makasih Ira!"
Dito (from side, grinning): "Tenang Bram, aku tadi juga error 3 kali. Haha!"
MOOD: Friendly help, learning from mistakes, teamwork
SIZE: 800x600 pixels
FORMAT: PNG, clean background
```

---

## 1.9 LATIHAN MANDIRI

### SOLVED PROBLEM 1.14 ⭐

**Soal:** Jelaskan apa yang akan ditampilkan oleh program berikut:
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Baris 1\n";
    cout << "Baris 2" << endl;
    cout << "Baris 3";
    return 0;
}
```

**Penyelesaian:**

Program akan menampilkan:
```
Baris 1
Baris 2
Baris 3
```

**Penjelasan:**
- **Baris 1:** `\n` membuat newline, jadi "Baris 1" diikuti baris baru
- **Baris 2:** `endl` juga membuat newline, jadi "Baris 2" diikuti baris baru
- **Baris 3:** Tidak ada `\n` atau `endl`, tapi setelah program selesai, cursor tetap di akhir "Baris 3"

**Catatan:** `\n` dan `endl` fungsinya sama (newline), tapi:
- `\n` lebih cepat (tidak flush buffer)
- `endl` lebih lambat (flush buffer, memastikan output langsung tampil)
- Untuk program sederhana, perbedaannya tidak signifikan

---

### SOLVED PROBLEM 1.15 ⭐

**Soal:** Apa output dari program ini?
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "C:\\Users\\Admin\\Documents" << endl;
    cout << "Dia berkata: \"Selamat pagi\"" << endl;
    return 0;
}
```

**Penyelesaian:**

Output:
```
C:\Users\Admin\Documents
Dia berkata: "Selamat pagi"
```

**Penjelasan:**
- `\\` di-escape menjadi satu `\` di output
- `\"` di-escape menjadi `"` di output
- Escape sequences diproses saat runtime, bukan ditampilkan as-is

---

### SOLVED PROBLEM 1.16 ⭐⭐

**Soal:** Buatlah program yang menampilkan informasi berikut dengan format rapi:
```
============================================
         YONIF 123/RAJAWALI
============================================
Komandan  : Letkol Inf. Arief Budiman
Wakil     : Mayor Inf. Bambang Sutrisno
Danki 1   : Kapten Inf. Cahyo Permadi
Danki 2   : Kapten Inf. Deni Setiawan
============================================
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "============================================" << endl;
    cout << "         YONIF 123/RAJAWALI" << endl;
    cout << "============================================" << endl;
    cout << "Komandan  : Letkol Inf. Arief Budiman" << endl;
    cout << "Wakil     : Mayor Inf. Bambang Sutrisno" << endl;
    cout << "Danki 1   : Kapten Inf. Cahyo Permadi" << endl;
    cout << "Danki 2   : Kapten Inf. Deni Setiawan" << endl;
    cout << "============================================" << endl;
    
    return 0;
}
```

*Listing 1.10: Program informasi Yonif*

**Tips Formatting:**
- Gunakan spasi untuk alignment
- Hitung jumlah karakter `=` agar simetris
- Untuk centering, hitung (total width - text length) / 2
- Contoh: `YONIF 123/RAJAWALI` = 18 karakter, border = 44 karakter
  - Leading spaces = (44 - 18) / 2 = 13 spasi

---

### SOLVED PROBLEM 1.17 ⭐⭐

**Soal:** Identifikasi dan perbaiki semua error dalam program berikut:
```cpp
include <iostream>
using namespace std

int main() 
    cout << Hello World << endl
    return 0
```

**Penyelesaian:**

**Error yang ditemukan:**

1. **Baris 1:** `include <iostream>` → harus `#include <iostream>`
2. **Baris 2:** `using namespace std` → harus `using namespace std;`
3. **Baris 4:** Missing opening brace `{` after `main()`
4. **Baris 5:** `Hello World` → harus `"Hello World"` (string literal)
5. **Baris 5:** Missing semicolon `;` at end
6. **Baris 6:** Missing semicolon `;` at end
7. **Missing:** Closing brace `}` at end

**Program yang benar:**
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World" << endl;
    return 0;
}
```

**Jenis Error:**
- Error 1, 2, 5, 6, 7: **Syntax error** (missing characters)
- Error 3, 4: **Syntax error** (missing braces)

Semua error ini adalah **compile-time error** yang akan ditangkap oleh compiler.

---

### SOLVED PROBLEM 1.18 ⭐⭐

**Soal:** Buatlah program yang menampilkan menu sistem informasi:
```
+----------------------------+
|   SISTEM INFORMASI TARUNA  |
+----------------------------+
| 1. Data Pribadi            |
| 2. Nilai Akademik          |
| 3. Laporan Kedisiplinan    |
| 4. Keluar                  |
+----------------------------+
Pilih menu (1-4):
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "+----------------------------+" << endl;
    cout << "|   SISTEM INFORMASI TARUNA  |" << endl;
    cout << "+----------------------------+" << endl;
    cout << "| 1. Data Pribadi            |" << endl;
    cout << "| 2. Nilai Akademik          |" << endl;
    cout << "| 3. Laporan Kedisiplinan    |" << endl;
    cout << "| 4. Keluar                  |" << endl;
    cout << "+----------------------------+" << endl;
    cout << "Pilih menu (1-4): ";
    
    return 0;
}
```

*Listing 1.11: Program menu sistem informasi*

**Catatan:**
- Baris terakhir tidak pakai `endl` agar cursor tetap di samping prompt
- Semua baris menu harus sama panjang (28 karakter di dalam box)
- Tambahkan spasi trailing jika perlu agar alignment benar

**Perhitungan Width:**
```
Border: | + 26 karakter + | = 28
Menu 1: | + 1 spasi + "1. Data Pribadi" (14 char) + 11 spasi + | = 28
Menu 2: | + 1 spasi + "2. Nilai Akademik" (17 char) + 8 spasi + | = 28
dst.
```

---

### SOLVED PROBLEM 1.19 ⭐⭐⭐

**Soal:** Buatlah program yang menampilkan tabel perbandingan pangkat TNI dengan format seperti ini:
```
+----------+-------------------+------------------+
| ANGKATAN |  PERWIRA TINGGI   | PERWIRA MENENGAH |
+----------+-------------------+------------------+
| AD       | Jenderal          | Mayor Jenderal   |
|          | Letnan Jenderal   | Brigadir Jenderal|
+----------+-------------------+------------------+
| AU       | Marsekal          | Marsekal Muda    |
|          | Marsekal Madya    | Marsekal Pertama |
+----------+-------------------+------------------+
```

(Tabel disederhanakan untuk contoh)

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    // Header
    cout << "+----------+-------------------+------------------+" << endl;
    cout << "| ANGKATAN |  PERWIRA TINGGI   | PERWIRA MENENGAH |" << endl;
    cout << "+----------+-------------------+------------------+" << endl;
    
    // Data TNI AD
    cout << "| AD       | Jenderal          | Mayor Jenderal   |" << endl;
    cout << "|          | Letnan Jenderal   | Brigadir Jenderal|" << endl;
    cout << "+----------+-------------------+------------------+" << endl;
    
    // Data TNI AU
    cout << "| AU       | Marsekal          | Marsekal Muda    |" << endl;
    cout << "|          | Marsekal Madya    | Marsekal Pertama |" << endl;
    cout << "+----------+-------------------+------------------+" << endl;
    
    return 0;
}
```

*Listing 1.12: Program tabel pangkat TNI*

**Penjelasan:**
- Setiap cell harus dihitung panjangnya agar alignment benar
- Gunakan spasi untuk padding
- Kolom 1 (ANGKATAN): 10 karakter
- Kolom 2 (PERWIRA TINGGI): 19 karakter
- Kolom 3 (PERWIRA MENENGAH): 18 karakter

**Tips:**
- Tulis 1 baris dulu, test alignment-nya
- Copy-paste untuk baris berikutnya
- Hitung manual jumlah spasi yang dibutuhkan
- Jika alignment berantakan, cek jumlah spasi dan karakter

**Advanced:** Di pertemuan mendalam (Pertemuan 3), kita akan belajar cara formatting yang lebih mudah menggunakan manipulator seperti `setw()`.

---

### SOLVED PROBLEM 1.20 ⭐⭐⭐

**Soal:** Buatlah program yang menampilkan "animasi" loading sederhana menggunakan escape sequence `\r` (carriage return):
```
Loading.
Loading..
Loading...
Selesai!
```

Petunjuk: `\r` akan mengembalikan cursor ke awal baris tanpa newline.

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Loading.  \r";  // \r kembali ke awal baris
    cout << "Loading.. \r";
    cout << "Loading...\r";
    cout << "Selesai!  " << endl;
    
    return 0;
}
```

*Listing 1.13: Program loading animation dengan \r*

**Catatan:**
- Dalam praktik, program akan tereksekusi terlalu cepat sehingga kita tidak melihat efek "animasi"
- Untuk melihat efek sesungguhnya, perlu delay (akan dipelajari di pertemuan lanjutan)
- Spasi trailing `"Loading.  "` penting untuk "menghapus" karakter sebelumnya

**Penjelasan `\r` vs `\n`:**
- `\n`: Pindah ke baris baru (newline)
- `\r`: Kembali ke awal baris yang sama (carriage return)
- `\r` biasanya digunakan untuk:
  - Progress bar
  - Loading animation
  - Update nilai di baris yang sama

**Preview dengan delay (konsep, belum diajarkan):**
```cpp
// HANYA UNTUK KONSEP - akan dipelajari di pertemuan lanjutan
#include <iostream>
#include <windows.h> // untuk Sleep()
using namespace std;

int main() {
    cout << "Loading.  ";
    Sleep(500); // delay 500ms
    cout << "\rLoading.. ";
    Sleep(500);
    cout << "\rLoading...";
    Sleep(500);
    cout << "\rSelesai!  " << endl;
    
    return 0;
}
```

---

### SOLVED PROBLEM 1.21 ⭐⭐⭐

**Soal:** Buatlah program yang menampilkan "sertifikat" sederhana:
```
╔══════════════════════════════════════════╗
║                                          ║
║         DATAFORCE MILITARY ACADEMY       ║
║              SERTIFIKAT                  ║
║                                          ║
║     Diberikan kepada:                    ║
║         DITO PRASETYO                    ║
║                                          ║
║     Telah menyelesaikan:                 ║
║     Pertemuan 1 - Pengenalan C++         ║
║                                          ║
║     Tanggal: 15 Februari 2026            ║
║                                          ║
╚══════════════════════════════════════════╝
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    // Menggunakan box-drawing characters
    cout << "╔══════════════════════════════════════════╗" << endl;
    cout << "║                                          ║" << endl;
    cout << "║         DATAFORCE MILITARY ACADEMY       ║" << endl;
    cout << "║              SERTIFIKAT                  ║" << endl;
    cout << "║                                          ║" << endl;
    cout << "║     Diberikan kepada:                    ║" << endl;
    cout << "║         DITO PRASETYO                    ║" << endl;
    cout << "║                                          ║" << endl;
    cout << "║     Telah menyelesaikan:                 ║" << endl;
    cout << "║     Pertemuan 1 - Pengenalan C++         ║" << endl;
    cout << "║                                          ║" << endl;
    cout << "║     Tanggal: 15 Februari 2026            ║" << endl;
    cout << "║                                          ║" << endl;
    cout << "╚══════════════════════════════════════════╝" << endl;
    
    return 0;
}
```

*Listing 1.14: Program sertifikat dengan box-drawing characters*

**Catatan Teknis:**
- Karakter ╔ ║ ╚ dll adalah **box-drawing characters** dari extended ASCII/Unicode
- Di Code::Blocks Windows, bisa langsung pakai karakter ini
- Di Linux/Mac, mungkin perlu set encoding UTF-8
- Alternatif: pakai `+`, `-`, `|` untuk kompatibilitas maksimal

**Versi Kompatibel (ASCII biasa):**
```cpp
cout << "+------------------------------------------+" << endl;
cout << "|                                          |" << endl;
cout << "|         DATAFORCE MILITARY ACADEMY       |" << endl;
// ... dst
cout << "+------------------------------------------+" << endl;
```

---

### SOLVED PROBLEM 1.22 ⭐⭐⭐

**Soal:** Buatlah program yang menampilkan diagram organisasi sederhana menggunakan ASCII art:
```
              KOMANDAN
                 |
      +----------+----------+
      |          |          |
   DANKI 1    DANKI 2    DANKI 3
      |          |          |
   10 prajurit   12 prajurit   11 prajurit
```

**Penyelesaian:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "              KOMANDAN" << endl;
    cout << "                 |" << endl;
    cout << "      +----------+----------+" << endl;
    cout << "      |          |          |" << endl;
    cout << "   DANKI 1    DANKI 2    DANKI 3" << endl;
    cout << "      |          |          |" << endl;
    cout << "   10 prajurit   12 prajurit   11 prajurit" << endl;
    
    return 0;
}
```

*Listing 1.15: Program diagram organisasi ASCII*

**Penjelasan:**
- Diagram hierarki ditampilkan menggunakan karakter `|`, `+`, dan `-`
- Perlu teliti dalam menghitung spasi agar alignment benar
- Setiap "node" harus sejajar dengan "edge" yang menghubungkannya

**Tips Membuat ASCII Diagram:**
1. Gambar dulu di text editor/notepad
2. Hitung jumlah spasi dari margin kiri
3. Pastikan alignment vertical (gunakan monospace font)
4. Copy paste ke string C++ satu per satu
5. Test dan adjust jika perlu

**Challenge:** Coba modifikasi untuk menampilkan struktur organisasi satuan kalian!

---

## RINGKASAN

| Konsep | Penjelasan Singkat |
|--------|-------------------|
| **Pemrograman** | Proses menulis instruksi untuk komputer menyelesaikan masalah |
| **Algoritma** | Urutan langkah logis untuk menyelesaikan masalah (finite, definite, effective) |
| **Paradigma Pemrograman** | Cara pandang/pendekatan dalam menulis program (prosedural, OOP, fungsional, dll) |
| **C++** | Bahasa multi-paradigma, compiled, high-performance, dikembangkan oleh Bjarne Stroustrup |
| **Struktur Program C++** | `#include` → `using namespace` → `int main()` → statements → `return 0` |
| **Preprocessor Directive** | Instruksi yang diproses sebelum kompilasi, diawali `#` (contoh: `#include`) |
| **cout dan endl** | `cout` untuk output, `<<` operator insertion, `endl` untuk newline |
| **Komentar** | `//` untuk single-line, `/* */` untuk multi-line |
| **Kompilasi** | Proses: Preprocessing → Compilation → Linking → Execution |
| **Compiler** | Program yang mengubah source code menjadi machine code (GCC, Clang, MSVC) |
| **IDE** | Integrated Development Environment - gabungan editor, compiler, debugger |
| **Code::Blocks** | IDE yang kita gunakan, include MinGW GCC compiler |
| **Compile Error** | Error saat kompilasi karena syntax salah, harus diperbaiki sebelum run |
| **Runtime Error** | Error saat eksekusi karena logical error, program crash atau hasil salah |
| **Escape Sequences** | Karakter khusus: `\n` (newline), `\t` (tab), `\\` (backslash), `\"` (quote) |
| **Debugging** | Proses mencari dan memperbaiki bug menggunakan breakpoint, step, watch |

---

## REFERENSI VIDEO PEMBELAJARAN

### Video Bahasa Indonesia

1. **Belajar C++ [Dasar] - 01 - Pengenalan C++**
   - Channel: Kelas Terbuka
   - URL: https://www.youtube.com/watch?v=WtbW_qYAGw8
   - Durasi: 13:36
   - Topik: Pengenalan bahasa C++, sejarah, dan karakteristik
   - Catatan: Penjelasan sangat jelas tentang mengapa belajar C++ dan sejarahnya

2. **Belajar C++ [Dasar] - 02 - Instalasi Dev C++**
   - Channel: Kelas Terbuka
   - URL: https://www.youtube.com/watch?v=YAOV5RrUk-c
   - Durasi: 10:52
   - Topik: Instalasi IDE untuk C++ (Dev C++, prinsipnya sama dengan Code::Blocks)
   - Catatan: Meskipun menggunakan Dev C++, konsep instalasi compiler sama untuk Code::Blocks

3. **Belajar C++ [Dasar] - 03 - Program Pertama Hello World**
   - Channel: Kelas Terbuka
   - URL: https://www.youtube.com/watch?v=3MXtPorganization
   - Durasi: 15:24
   - Topik: Membuat program Hello World pertama, struktur dasar program C++
   - Catatan: Penjelasan detail tentang #include, main(), cout, dan return 0

4. **Algoritma dan Flowchart - Dasar Pemrograman**
   - Channel: Guntur Budi
   - URL: https://www.youtube.com/watch?v=vBLCdKEH1Fw
   - Durasi: 21:45
   - Topik: Konsep algoritma, flowchart, dan pseudocode dengan contoh kasus
   - Catatan: Penjelasan lengkap dengan contoh real-world problem solving

5. **Install Code::Blocks di Windows 10/11**
   - Channel: Sibakua Channel
   - URL: https://www.youtube.com/watch?v=qJfHRA_XQK0
   - Durasi: 8:47
   - Topik: Tutorial instalasi Code::Blocks lengkap di Windows
   - Catatan: Step-by-step dari download, install, sampai compile program pertama

### Video Bahasa Inggris (Opsional)

6. **C++ Tutorial for Beginners - Full Course**
   - Channel: freeCodeCamp.org
   - URL: https://www.youtube.com/watch?v=vLnPwxZdW4Y
   - Durasi: 4:01:19 (gunakan bagian awal: 00:00-30:00 untuk dasar-dasar)
   - Topik: Complete C++ tutorial dari dasar hingga advanced
   - Catatan: Bagian 00:00-30:00 mencakup setup, Hello World, dan basic syntax. Sangat comprehensive untuk referensi tambahan
   - Topik: First C++ program, IDE setup
   - Catatan: Penjelasan dalam bahasa Inggris tapi sangat jelas dengan visual

7. **C++ Tutorial for Beginners - Full Course**
   - Channel: freeCodeCamp.org
   - URL: https://www.youtube.com/watch?v=VIDEO_ID_7
   - Durasi: 4:01:19 (FULL COURSE)
   - Topik: Complete C++ fundamentals
   - Catatan: Hanya perlu Part 1 (00:00-25:00) untuk Pertemuan 1 ini, sisanya untuk pertemuan selanjutnya

## SUPPLEMENTARY PROBLEMS

Berikut adalah 5 soal tambahan untuk latihan mandiri. Jawaban singkat diberikan di akhir.

### SUPPLEMENTARY PROBLEM 1

Apa perbedaan utama antara bahasa pemrograman **compiled** (seperti C++) dan **interpreted** (seperti Python)? Sebutkan 2 kelebihan dan 2 kekurangan masing-masing.

**Jawaban Singkat:**

**Compiled (C++):**
- Kelebihan:
  1. Sangat cepat saat eksekusi (sudah jadi machine code)
  2. Error terdeteksi saat kompilasi (compile-time checking)
- Kekurangan:
  1. Perlu compile ulang setiap kali kode berubah
  2. Executable platform-specific (Windows .exe tidak jalan di Linux)

**Interpreted (Python):**
- Kelebihan:
  1. Langsung run tanpa perlu compile
  2. Cross-platform (script yang sama jalan di berbagai OS)
- Kekurangan:
  1. Lebih lambat (di-interpret saat runtime)
  2. Error baru terdeteksi saat baris tersebut dieksekusi

---

### SUPPLEMENTARY PROBLEM 2

Jelaskan mengapa statement berikut menghasilkan error dan bagaimana memperbaikinya:
```cpp
cout << This is a test << endl;
```

**Jawaban Singkat:**

**Error:** `This is a test` bukan string literal yang valid.

**Alasan:** String literal harus diapit double quotes `" "`.

**Perbaikan:**
```cpp
cout << "This is a test" << endl;
```

---

### SUPPLEMENTARY PROBLEM 3

Buatlah algoritma dalam bentuk pseudocode untuk menentukan apakah seorang kadet lolos seleksi masuk DataForce Academy dengan kriteria:
- Nilai akademik minimal 80
- Tes fisik minimal 75
- Wawancara minimal 70
- Lolos jika SEMUA syarat terpenuhi

**Jawaban Singkat:**

```
ALGORITMA Seleksi_DataForce_Academy

INPUT:
    nilai_akademik (integer)
    nilai_fisik (integer)
    nilai_wawancara (integer)

PROSES:
    IF (nilai_akademik >= 80) AND (nilai_fisik >= 75) AND (nilai_wawancara >= 70) THEN
        status = "LOLOS"
    ELSE
        status = "TIDAK LOLOS"
    END IF

OUTPUT:
    Tampilkan status

END ALGORITMA
```

---

### SUPPLEMENTARY PROBLEM 4

Apa output dari program berikut? Jelaskan mengapa.
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "A\tB\tC" << endl;
    cout << "1\t2\t3" << endl;
    return 0;
}
```

**Jawaban Singkat:**

**Output:**
```
A       B       C
1       2       3
```

**Penjelasan:**
- `\t` adalah escape sequence untuk TAB (sekitar 8 spasi)
- Membuat alignment kolom seperti tabel
- `endl` membuat newline di akhir setiap baris

---

### SUPPLEMENTARY PROBLEM 5

Sebutkan 5 aplikasi di dunia nyata yang menggunakan C++, dan jelaskan mengapa C++ dipilih untuk aplikasi tersebut (minimal 1 alasan per aplikasi).

**Jawaban Singkat:**

1. **Game Engines (Unreal Engine, Unity)**
   - Alasan: Performa tinggi untuk real-time rendering dan physics simulation

2. **Web Browsers (Chrome, Firefox)**
   - Alasan: Kecepatan eksekusi untuk parsing HTML/CSS dan JavaScript engine

3. **Operating Systems (Windows, Linux kernel components)**
   - Alasan: Low-level access ke hardware dan memory management yang efisien

4. **Database Systems (MySQL, PostgreSQL)**
   - Alasan: Performa query yang cepat dan efisien untuk big data

5. **Aerospace & Defense Systems (Missile guidance, radar systems)**
   - Alasan: Reliability, real-time performance, dan kontrol hardware langsung

---

## REFERENSI BUKU

Berikut adalah referensi buku yang relevan untuk materi Pertemuan 01:

### Referensi Utama

1. **Deitel, P.J. & Deitel, H.M. (2016).** *C++ How to Program* (10th Ed.). Pearson Education. ISBN: 978-0134448237
   - **Bab Relevan:** Chapter 1 (Introduction to Computers and C++), Chapter 2 (Introduction to C++ Programming)
   - **Topik:** Pengenalan C++, struktur program dasar, input/output
   - **Catatan:** Sangat detail dengan banyak contoh program dan latihan

2. **Savitch, W. (2017).** *Problem Solving with C++* (10th Ed.). Pearson Education. ISBN: 978-0134448282
   - **Bab Relevan:** Chapter 1 (Introduction to Computers and C++ Programming)
   - **Topik:** Problem solving approach, algoritma, pengenalan C++
   - **Catatan:** Fokus pada problem-solving methodology yang sangat cocok untuk pemula

3. **Stroustrup, B. (2022).** *Programming: Principles and Practice Using C++* (3rd Ed.). Addison-Wesley Professional. ISBN: 978-0138308681
   - **Bab Relevan:** Chapter 1 (Computers, People, and Programming), Chapter 2 (Hello, World!)
   - **Topik:** Filosofi pemrograman, pengenalan C++ dari creator-nya sendiri
   - **Catatan:** Ditulis oleh pencipta C++, memberikan perspektif mendalam tentang desain bahasa

### Referensi Pendukung

4. **Gaddis, T. (2018).** *Starting Out with C++ from Control Structures to Objects* (9th Ed.). Pearson Education. ISBN: 978-0134498379
   - **Bab Relevan:** Chapter 1 (Introduction to Computers and Programming)
   - **Catatan:** Penjelasan sangat jelas untuk absolute beginner

5. **Lippman, S.B., Lajoie, J., & Moo, B.E. (2012).** *C++ Primer* (5th Ed.). Addison-Wesley Professional. ISBN: 978-0321714114
   - **Bab Relevan:** Chapter 1 (Getting Started)
   - **Catatan:** Reference book yang sangat comprehensive untuk C++

### Catatan Penggunaan

- **Untuk pemahaman konsep**: Baca Savitch Ch.1 dan Stroustrup Ch.1-2
- **Untuk contoh program**: Lihat Deitel Ch.1-2 yang memiliki ratusan contoh kode
- **Untuk referensi mendalam**: Gunakan Lippman sebagai reference book
- **Untuk latihan tambahan**: Gaddis memiliki banyak latihan bertahap yang cocok untuk practice

---

## License

This repository is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Commercial use is permitted, provided attribution is given to the author.

© 2026 Anindito
