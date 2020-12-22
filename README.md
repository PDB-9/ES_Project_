# Spoti.py

Repositori _git_ ini berisi kode sumber untuk aplikasi Spoti.py yang dibuat oleh **Kelompok 9**. Teknologi utama yang digunakan dalam pengembangan proyek ini adalah **Elasticsearch**. Proyek ini merupakan bagian dari mata kuliah Pengelolaan Data Besar Semester Ganjil 2021/2022, Fakultas Ilmu Komputer, Universitas Indonesia.

Anggota Kelompok 9:

1. Ali Yusuf - 1706044061
2. Maharani Eka Pratiwi - 1706043626
3. Reinaldy Rabbany - 1706043872
4. Roshani Ayu Pranasti - 1706026052

## Penjelasan Produk

Aplikasi yang dapat mengembalikan hasil lagu berdasarkan masukan yang diberikan oleh pengguna. Form yang ada pada halaman utama aplikasi dapat diisi oleh pengguna dan aplikasi akan mengembalikan hasil pencarian berdasarkan isi dari form tersebut. Aplikasi ini memanfaatkan data lagu Spotify yang dapat ditemukan pada tautan [ini](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks).

Tujuan pengembangan dari aplikasi Spoti.py, yaitu sebagai platform terpadu untuk memproses pencarian data lagu Spotify secara efektif.

_Live on_: https://spotipy.netlify.app/

Proyek ini menggunakan:

- Elasticsearch v7.10.0
- yarn v1.22.0
- Django v3.1.4 (Back-end)
- React (Front-end): react-scripts v4.0.1

## Docker Container (Elasticsearch + Django + React)

Jalankan perintah berikut untuk melakukan _clone repository_:

    git clone https://github.com/PDB-9/ES_Project.git
    cd ES_Project

Jalankan docker-compose

    docker-compose up

Untuk mengatasi masalah terbatasnya alokasi memori:

    wsl -d docker-desktop
    sysctl -w vm.max_map_count=262144

atau (untuk docker-desktop non WSL):

    docker-machine ssh
    sudo sysctl -w vm.max_map_count=262144

Untuk memasukan data:
    
    docker exec -it backend bash
    cd dataset
    python script.py

Elasticsearch: localhost:9200 (Node es03)

Django: localhost:8000

React: localhost:3000