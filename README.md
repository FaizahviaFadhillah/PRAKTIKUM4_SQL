## PRAKTIKUM4_SQL

`Nama  : Faizah Via Fadhillah`

`Nim   : 312210460`

`Kelas : TI22.A4`

# Tugas Praktikum

- TABEL Pegawai

![img.1](gambar/1.png)

1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000!

    Script 

    ```sql
    SELECT * FROM pegawai WHERE gaji <> 2000000 AND gaji <> 1250000;
    ```

    Output 

    ![img.2](gambar/2.png)

2. Tampilkan pegawai yang tunjangannya NUL!

    Script 

    ```sql
    SELECT * FROM pegawai WHERE tunjangan IS NULL;
    ```

    Output

    ![img.3](gambar/3.png)

3. Tampilkan pegawai yang tunjangannya tidak NULL!

    Script 

    ```sql
    SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;
    ```

    Output 

    ![img.4](gambar/4.png)

4. Tampilkan/hitung jumlah baris/record tabel pegawai!

    Script 

    ```sql
    SELECT COUNT(*) AS jumlah_baris FROM pegawai;
    ```

    Output

    ![img.5](gambar/5.png)

5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

    Script 

    ```sql
    SELECT SUM(gaji) AS total_gaji FROM pegawai;
    ```

    Output 

    ![img.6](gambar/6.png)

6. Tampilkan/hitung jumlah rata-rata gaji pegawai!

    Script 

    ```sql
    SELECT AVG(gaji) AS rata_gaji FROM pegawai;
    ```

    Output

    ![img.7](gambar/7.png)

7. Tampilkan gaji terkecil!

    Script 

    ```sql
    SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;
    ```

    Output 

    ![img.8](gambar/gaji%20kecil.png)

8.  Tampilkan gaji terbesar!

    Script 

    ```sql
     SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;
    ```

    Output 

    ![img.9](gambar/8.png)

- TABEL Hewan

![img.10](gambar/9.png)

1. Tampilkan jumlah hewan yang dimiliki setiap owner!

    Script 

    ```sql
     SELECT owner, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY owner;
    ```

    Output 

    ![img.11](gambar/10.png)

2. Tampilkan jumlah hewan berdasarkan spesies!

    Script 

    ```sql
    SELECT species, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species;
    ```

    Output

    ![img.12](gambar/11.png)

3. Tampilkan jumlah hewan berdasarkan jenis kelamin!

    Script 

    ```sql
    SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY sex;
    ```

    Output 

    ![img.13](gambar/12.png)

4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin!

    Script 

    ```sql
    SELECT species,sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species,sex;
    ```

    Output 

    ![img.14](gambar/13.png)

5. Tampilkan jumlah hewan berdasarkan spesies (cat dan dog saja) dan jenis kelamin!

    Script 

    ```sql
     SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE species IN ('Cat', 'Dog') GROUP BY species, sex;
    ```

    Output 

    ![img.15](gambar/14.png)

6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja!

    Script 

    ```sql 
    SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE sex IN('f','m') 
    GROUP BY sex;
    ```

    Output 

    ![img.16](gambar/15.png)


# Kesimpulan 

Query filtering adalah sebuah proses menyaring atau memfilter data dari basis data berdasarkan kriteria tertentu menggunakan perintah query dalam bahasa SQL. Tujuan utamanya adalah membatasi atau mengambil subset data yang sesuai dengan kondisi yang ditentukan. Dengan menggunakan query filtering ini, Kita dapat menentukan berbagai jenis kondisi seperti kesamaan `(equal)`, ketidaksamaan `(not equal)`, rentang nilai `(range)`, kondisi logis `(AND, OR)`, atau kombinasi kondisi lainnya. Dengan mengatur kondisi yang sesuai, Anda dapat mengambil hanya data yang relevan atau yang memenuhi persyaratan tertentu.



