Nama : Whinta Virginia Putri 

Nim : 210411100047



Tools:

1. Install Postgres
2. Install Power BI
3. Install XAMPP

4. Create Account ElephantSQL

   

Tahapan-tahapan untuk mengumpulkan data dari beberapa sumber:

- ElephantSQL:

  1. membuat akun elephant dengan nama "pendata" yang nantinya digunakan untuk server cloud

  ![](Screenshots\Screenshot (791).png)

     2. Membuat Instance dengan nama "Pendatairis"

        ![](Screenshots\Screenshot (792).png)

- Postgres / pgadmin :

  - Setelah instalasi postgres, lalu jalankan postgres / pgadmin

    1. Import data dari github ke postgres :

       - buat database dengan nama "dbiris"

       - lalu buat table "iris" dengan cara klik kanan pada table dan pilih query tool

       - lalu salin sql dari link github berikut : https://gist.github.com/faustofjunqueira/ba97008616148653a9c633c066edaba9

       - buka query tool lalu paste sql yang sudah disalin setelah itu klik Excute.

         ![](Screenshots\image-20230302153922040.png)

       - Data telah selesai diimport untuk menampilkannya di query tool lalukan perintah sql "select * from public."iris"" dan klik Excute

         ![](Screenshots\image-20230302154255997.png)

         

    2. Menghubungkan Postgres dengan server ElephantSQL:

       - klik kanan pada server lalu pilih register dan pilih server 

       - Setelah itu isi name dengan nama instance yang dibuat di ElephantSQL, lalu klik Connection dan isi host name dengan link server di instance, isi maintenance database dan username dengan User & Default database di instance yang telah dibuat dan terakhir isi password sesuai password yang diberi di instance jika sudah diisi klik save.

         ![](Screenshots\Screenshot (793).png)

         ![](Screenshots\Screenshot (795).png)

       - Sebelum mengimport data carilah nama database yang sesuai dengan User & Default database diinstance yang dibuat.

         ![](Screenshots\Screenshot (798).png)

       - Lalu pilih schemas, pilih public setelah itu pilih table dan klik kanan table dan pilih query tool

       - setelah itu salin sql dari link github berikut : https://gist.github.com/faustofjunqueira/ba97008616148653a9c633c066edaba9

       - setelah salin sql kembali ke query tool dan paste sql yang sudah disalin setelah itu klik excute.

       - Data telah berhasil di import, selanjutnya untuk melihat data tulis perintah sql "select * from public."iris""

         ![](Screenshots/image-20230302161611434.png)

         

    3. Membuat server local di Postgres:

       - klik kanan pada server lalu pilih register dan pilih server 

       - setelah itu isi name "localhostpendata", lalu pilih connection dan isi hostname/address dengan "localhost" lalu isi password dengan password postgres.

         ![](Screenshots\image-20230302162311254.png)

         ![](Screenshots\image-20230302163022253.png)

       - Server local postgres telah berhasil dibuat.

         ![](Screenshots\image-20230302163349479.png)

  

- Mysql : 

  Import csv ke mysql, sebelum melakukan import ke mysql lakukan export data iris dari postgres,

  dengan cara klik kanan pada table iris lalu pilih import/export data, lalu centang/pilih export dan beri nama file lalu pilih csv jika sudah klik ok. Maka file csv sudah tersimpan.

  ![](Screenshots\image-20230302164631305.png)

  1. Nyalakan XAMPP dan klik start pada apache serta mysql

     ![](Screenshots\image-20230302172905896.png)

  2. lalu ke web browser dan tulis perintah "http://localhost/phpmyadmin/"

  3. buatlah database "dbiris"

     ![](Screenshots\image-20230302173156947.png)

  4. lalu pilih import dan pilih file csv yang akan di import setelah itu ganti format jadi csv dan klik import

     ![](Screenshots\image-20230302173458283.png)

  5.  Data telah behasil diimport ke mysql

     ![](Screenshots\image-20230302173648972.png)

- Power BI :

  1. Import csv ke Power BI:

     sebelum melakukan import ke Power BI lakukan export data iris dari postgres,

     dengan cara klik kanan pada table iris lalu pilih import/export data, lalu centang/pilih export dan beri nama file lalu pilih csv jika sudah klik ok. Maka file csv sudah tersimpan.

     ![](Screenshots\image-20230302164631305.png)

     ![](Screenshots\Screenshot (806).png)

     - Jalankan Power BI pada menu home pilih get data lalu klik more, pilih Text/CSV dan klik connect.

       ![](Screenshots\image-20230302165123994.png)

     - Setelah memilih file csv setalah itu akan ada tampilan seperti dibawah ini dan klik load

       ![](Screenshots\image-20230302165701467.png)

     - Lalu setelah berhasil diimport maka tampilkan data dalam bentuk diagram.

       ![](Screenshots\image-20230302170202787.png)

       

  2. Mengkoneksi Postgres ke Power BI, dan Import Data iris dari Postgres ke Power BI:

     - Jalankan Power BI pada menu home pilih get data lalu klik more, pilih PostgreSQL Database dan klik connect.

       ![](Screenshots\image-20230302170822605.png)

     - isi server dengan server instance yang sudah dihubungkan dengan postgresql tadi serta nama database nya

       ![](Screenshots\Screenshot (812).png)

     - isi username dengan User & Default database instance serta password yang telah diberikan diinstance lalu klik connect.

       ![](Screenshots\image-20230302171415739.png)

     - setelah tampil seperti dibawah ini centang pada table public.iris lalu klik load 

       ![](Screenshots\image-20230302171537087.png)

     - Data telah berhasil diimport tampilkan dalam bentuk diagram

       ![](Screenshots\image-20230302175750176.png)

  3. Mengkoneksi Mysql ke Power BI, dan Import Data iris dari Mysql ke Power BI:
  
     sebelum mengkoneksikan mysql ke power bi download mysql installer (https://dev.mysql.com/downloads/connector/net/)
  
     - Jalankan Power BI pada menu home pilih get data lalu klik more, pilih MySQL Database dan klik connect.
  
       ![](Screenshots\image-20230302174023997.png)
  
     - isi server dengan "localhost:3306" (3306 adalah port) lalu isi database dengan nama database yang sudah dibuat
  
       ![](Screenshots\image-20230302174548148.png)
  
     - pilih Database lalu isi Username "root" lalu isi password mysql/phpmyadmin dan klik connect.
  
       ![](Screenshots\image-20230302175008404.png)
  
     - setelah tampilannya seperti di bawah ini lalu centang di dbiris.iris (database dimysql) dan klik load
  
       ![](Screenshots\image-20230302175303603.png)
  
     - Data telah berhasil diimport centang setiap colom untuk menampilkannya
  
       ![](Screenshots\image-20230302175630116.png)
  



Berikut adalah cara mengumpilkan data dari beberapa sumber. Terimakasih telah membaca:))

Semoga bermanfaat...