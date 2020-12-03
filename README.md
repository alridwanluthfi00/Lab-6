# Nama   : Luthfi Al Ridwan
# NIM    : 312010112  
# Kelas  : TI.20.A.1
# Matkul : Bahasa Pemrograman

# Lab 6

![Screenshot (188)](https://user-images.githubusercontent.com/73066008/100971283-2267d380-3569-11eb-9df0-cabdedc2b0fd.png)

__Berikut input code nya__ :

    from data import data



    print("PROGRAM MENAMPILKAN DAFATR NILAI MAHASISWA")
 
    while True:
    print("")
    c =input("(L)lihat, (T)ambah, (U)bah, (H)apus, (K)eluar : ")
   
    if c.lower() == 't':
        print("=======Tambah Data=======")
        nama = input("Nama                :  ")
        nim = input("Nim                 :  ")
        tugas = int(input("Masukan Nilai Tugas :  "))
        uts = int(input("Masukan Nilai UTS   :  "))
        uas = int(input("Masukan Nilai UAS   :  "))
        akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
        data[nama] = nim, tugas, uts, uas, akhir
   
    elif c.lower() == 'u':
        
        print('=======Ubah Data Mahasiswa=======')
        nama = input('Nama                :  ')
       
       if nama in data.keys():
            nim = input('Nim                 :  ')
            tugas = int(input("Masukan Nilai Tugas :  "))
            uts = int(input("Masukan Nilai UTS   :  "))
            uas = int(input("Masukan Nilai UAS   :  "))
            akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
            data[nama] = nim, tugas, uts, uas, akhir
       
       else:
            print("Data Nilai Tidak Ada".format(nama))
            
    elif c.lower() == 'l':
        print("=======Daftar Nilai Mahasiswa=======")
        print("================================================================================================")
        print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
        print("================================================================================================")
        i = 0
        for x in data.items():
            i += 1
            print(
                " | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |".format(x[0], x[1][0], x[1][1],
                                                                                                x[1][2], x[1][3],
                                                                                                x[1][4], i))
            print("============================================================================================")

    elif c.lower() == 'h':
        print("=======Hapus Data Mahasiswa=======")
        nama = input("Nama :  ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data Nilai Tidak Ada".format(nama))

    elif c.lower() == 'k':
        print("Keluar")
        break
        
1. Langkah pertama yang kita lakukan adalah membuat variable list kosong.

        from data import data
        
2. Setelah itu buat kondisi perulangan dan statement yang akan dijalankan ketika perulangan terjadi. 

       print("PROGRAM MENAMPILKAN DAFATR NILAI MAHASISWA")
       while True:
          print("")
          c =input("(L)lihat, (T)ambah, (U)bah, (H)apus, (K)eluar : ")
          
3. Berikutnya tambahkan input code fungsi tambahkan.

        if c.lower() == 't':
        print("=======Tambah Data=======")
        
              nama = input("Nama                :  ")
              nim = input("Nim                 :  ")
              tugas = int(input("Masukan Nilai Tugas :  "))
              uts = int(input("Masukan Nilai UTS   :  "))
              uas = int(input("Masukan Nilai UAS   :  "))
              akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
              data[nama] = nim, tugas, uts, uas, akhir
              
 4. Tambahkan input code fungsi ubah.
 
         elif c.lower() == 'u':
         print('=======Ubah Data Mahasiswa=======')
                  nama = input('Nama                :  ')
                  if nama in data.keys():
                      nim = input('Nim                 :  ')
                      tugas = int(input("Masukan Nilai Tugas :  "))
                      uts = int(input("Masukan Nilai UTS   :  "))
                      uas = int(input("Masukan Nilai UAS   :  "))
                      akhir = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
                      data[nama] = nim, tugas, uts, uas, akhir
                  else:
                      print("Data Nilai Tidak Ada".format(nama))
                      
 5. Tambahkan input code fungsi tampilkan.
 
        elif c.lower() == 'l':
        print("=======Daftar Nilai Mahasiswa=======")
                  print("================================================================================================")
                  print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
                  print("================================================================================================")
                  i = 0
                  for x in data.items():
                    i += 1
                    print(
                      " | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |".format(x[0], x[1][0], x[1][1],
                                                                                                      x[1][2], x[1][3],
                                                                                                      x[1][4], i))
                    print("============================================================================================")
                    
                    
 6. Tambahkan input code fungsi hapus.
 
        elif c.lower() == 'h':
        print("=======Hapus Data Mahasiswa=======")
            nama = input("Nama :  ")
            if nama in data.keys():
              del data[nama]
            else:
              print("Data Nilai Tidak Ada".format(nama))
              
 7. Tambahkan input code fungsi keluar.
 
        elif c.lower() == 'k':
        print("Keluar")
              break
             
 __Berikut output code nya__:
 
 ![Screenshot (190)](https://user-images.githubusercontent.com/73066008/100973786-c784ab00-356d-11eb-807c-810897197e8b.png)
 
 
        
