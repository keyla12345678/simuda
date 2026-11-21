

const form = document.getElementById("formPesanan");

form.addEventListener("submit", function(event) {
    event.preventDefault();

    const nama = document.getElementById("nama").value;
    const alamat = document.getElementById("alamat").value;
    const kategori = document.getElementById("kategori").value;
    const detail = document.getElementById("detail").value;

    let total = 0;

    keranjangSiMUDA.forEach(function(produk) {
        const hargaAngka = Number(
            produk.harga.replace(/[^0-9]/g, "")
        );

        total += hargaAngka;
    });

    
// Menampilkan informasi status pesanan
document.getElementById("isiStatusPesanan").innerHTML = `
    <h3>Pesanan Berhasil Dibuat!</h3>
    <p><strong>Nama:</strong> ${nama}</p>
    <p><strong>Alamat:</strong> ${alamat}</p>
    <p><strong>Kategori:</strong> ${kategori}</p>
    <p><strong>Detail Pesanan:</strong> ${detail}</p>
    <p><strong>Total Belanja:</strong> Rp${total.toLocaleString("id-ID")}</p>
    <p><strong>Status:</strong> Menunggu Diproses</p>
`;


        form.reset();

    // Mengosongkan keranjang setelah pesanan berhasil
keranjangSiMUDA = [];

// Mengosongkan tampilan keranjang
document.getElementById("isiKeranjang").innerHTML = "";

// Mengatur ulang total keranjang
document.getElementById("totalKeranjang").textContent = "Total: Rp0";

// Menyembunyikan keranjang
document.getElementById("halamanKeranjang").style.display = "none";

    // Menyembunyikan formulir pemesanan
    document.querySelector(".pesanan").style.display = "none";

    // Menampilkan halaman status pesanan
    document.getElementById("halamanStatus").style.display = "block";

    // Mengarahkan tampilan ke halaman status
    document.getElementById("halamanStatus").scrollIntoView({
        behavior: "smooth"
    });

});


// ===============================
// FUNGSI HALAMAN LOGIN DAN REGISTRASI
// ===============================

const halamanLogin = document.getElementById("halamanLogin");
const halamanRegistrasi = document.getElementById("halamanRegistrasi");
const halamanUtama = document.getElementById("halamanUtama");

// Tombol menuju halaman registrasi
document.getElementById("tombolRegistrasi").addEventListener("click", function() {
    halamanLogin.style.display = "none";
    halamanRegistrasi.style.display = "block";
});

// Tombol kembali ke halaman login
document.getElementById("tombolKembaliLogin").addEventListener("click", function() {
    halamanRegistrasi.style.display = "none";
    halamanLogin.style.display = "block";
});

// Menyimpan akun contoh selama halaman dibuka
let akunSiMUDA = null;
let alamatProfilSiMUDA = "";
// Proses registrasi
document.getElementById("formRegistrasi").addEventListener("submit", function(event) {
    event.preventDefault();

    const nama = document.getElementById("daftarNama").value;
    const telepon = document.getElementById("daftarTelepon").value;
    const email = document.getElementById("daftarEmail").value;
    const password = document.getElementById("daftarPassword").value;

    akunSiMUDA = {
        nama: nama,
        telepon: telepon,
        email: email,
        password: password
    };

    alert("PENDAFTARAN BERHASIL!\nSilakan masuk menggunakan akun kamu.");

    halamanRegistrasi.style.display = "none";
    halamanLogin.style.display = "block";

    document.getElementById("formRegistrasi").reset();
});

// Proses login contoh
document.getElementById("formLogin").addEventListener("submit", function(event) {
    event.preventDefault();

    const username = document.getElementById("loginUser").value;
    const password = document.getElementById("loginPassword").value;

    if (akunSiMUDA !== null &&
        (username === akunSiMUDA.email || username === akunSiMUDA.telepon) &&
        password === akunSiMUDA.password) {

        alert("LOGIN BERHASIL! Selamat datang di SiMUDA, " + akunSiMUDA.nama + ".");

        halamanLogin.style.display = "none";
        halamanUtama.style.display = "block";

    } else {
        alert("Akun tidak ditemukan atau password salah. Silakan daftar terlebih dahulu.");
    }
});

// ===============================

// ===============================
// DATA PRODUK DAN LAYANAN SiMUDA
// ===============================

const dataProduk = {
    "Sembako": [
    {
        nama: "Beras Fortune 5 Kg",
        harga: "Rp75.000",
        gambar: "https://arti-assets.sgp1.cdn.digitaloceanspaces.com/renyswalayanku/products/2974882a-da3d-4468-b93b-b6aa65ac199e.jpg"
    },
    {
        nama: "Minyak Goreng Bimoli 1 Liter",
        harga: "Rp18.000",
        gambar: "https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full/86/MTA-3007416/bimoli_surabaya---bimoli-classic-minyak-goreng--1-l--botol-_full02.jpg"
    },
    {
        nama: "Gula Gulaku 1 Kg",
        harga: "Rp17.000",
        gambar: "https://down-id.img.susercontent.com/file/id-11134207-822wp-mmgmb0hz3car9b"
    },
    {
        nama: "Telur Ayam 1 Kg",
        harga: "Rp30.000",
        gambar: "https://down-id.img.susercontent.com/file/id-11134207-7rasa-m0vxk22qy230ba"
    }
],

    "Makanan": [
    {
        nama: "Nasi Goreng",
        harga: "Rp15.000",
        gambar: "https://images.unsplash.com/photo-1603133872878-684f208fb84b?w=600"
    },
    {
    nama: "Mi Ayam",
    harga: "Rp12.000",
    gambar: "https://commons.wikimedia.org/wiki/Special:FilePath/Mi_ayam_biasa.JPG"
},
        {
        nama: "Bakso",
        harga: "Rp15.000",
        gambar: "https://upload.wikimedia.org/wikipedia/commons/6/6e/Bakso_Indonesian_Meatball_Soup_from_Solo.jpg"
    },
    {
    nama: "Nasi Ayam",
    harga: "Rp18.000",
    gambar: "https://media-cdn.tripadvisor.com/media/photo-s/0d/30/9a/72/gotta-love-them-chicken.jpg"
}
],

   "Minuman": [
    {
        nama: "Air Mineral Aqua 600 ml",
        harga: "Rp5.000",
        gambar: "https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full/92/MTA-23441519/aqua_aqua_air_mineral_kemasan_botol_600_ml-_1_karton-_24_pcs_full01_eg9ng5lp.jpg"
    },
    {
        nama: "Es Teh Manis",
        harga: "Rp5.000",
        gambar: "https://www.jagel.id/api/listimage/v/Es-Teh-Manis-0-165629dea15695e0.jpg"
    },
    {
        nama: "Jus Alpukat",
        harga: "Rp12.000",
        gambar: "https://cdn-assets.jawapos.com/images/3/2025/03/23/jus-alpukat-1-355026812.jpg"
    },
    {
        nama: "Susu Kemasan Ultra Milk",
        harga: "Rp7.000",
        gambar: "https://down-id.img.susercontent.com/file/id-11134207-8224z-mjgntaafk3y931"
    }
],

    "Laundry": [
    {
        nama: "Cuci Pakaian 1 Kg",
        harga: "Rp7.000",
        gambar: "https://images.unsplash.com/photo-1517677208171-0bc6725a3e60?w=600"
    },
    {
        nama: "Cuci dan Setrika 1 Kg",
        harga: "Rp10.000",
        gambar: "https://images.unsplash.com/photo-1545173168-9f1947eebb7f?w=600"
    },
    {
        nama: "Setrika Pakaian 1 Kg",
        harga: "Rp6.000",
        gambar: "https://images.unsplash.com/photo-1489274495757-95c7c837b101?w=600"
    }
],

   "Kebersihan": [
    {
        nama: "Jasa Membersihkan Rumah",
        harga: "Mulai Rp75.000",
        gambar: "https://images.unsplash.com/photo-1581578731548-c64695cc6952?w=600"
    },
    {
        nama: "Jasa Membersihkan Kamar",
        harga: "Mulai Rp35.000",
        gambar: "https://images.unsplash.com/photo-1527515637462-cff94eecc1ac?w=600"
    },
    {
        nama: "Jasa Membersihkan Kamar Mandi",
        harga: "Mulai Rp40.000",
        gambar: "https://images.unsplash.com/photo-1620626011761-996317b8d101?w=600"
    }
],

    "Servis": [
    {
        nama: "Servis Mesin Cuci",
        harga: "Mulai Rp75.000",
        gambar: "https://images.unsplash.com/photo-1626806787461-102c1bfaaea1?w=600"
    },
    {
        nama: "Servis Kipas Angin",
        harga: "Mulai Rp35.000",
        gambar: "https://tukangbagus.com/web/image/461-3997bec8/Elektronik%20Rumah.png"
    },
    {
        nama: "Servis Televisi",
        harga: "Mulai Rp100.000",
        gambar: "https://images.unsplash.com/photo-1593784991095-a205069470b6?w=600"
    }
]
};

let keranjangSiMUDA = [];
// ===============================
// FUNGSI PILIH KATEGORI
// ===============================

function pilihKategori(namaKategori) {

    const daftarProduk = document.getElementById("daftarProduk");
    const judulKategori = document.getElementById("judulKategori");
    const isiProduk = document.getElementById("isiProduk");

    judulKategori.textContent = "Daftar " + namaKategori;

    isiProduk.innerHTML = "";

    dataProduk[namaKategori].forEach(function(produk) {

       isiProduk.innerHTML += `
    <div class="kartu-produk">

        ${produk.gambar ? `
            <img src="${produk.gambar}"
                 alt="${produk.nama}"
                 class="foto-produk">
        ` : ""}

        <h3>${produk.nama}</h3>

        <p>Harga: ${produk.harga}</p>

        <button type="button"
            onclick="pilihProduk('${namaKategori}', '${produk.nama}')">
            Pilih Produk
        </button>

    </div>
`;

    });

    daftarProduk.style.display = "block";

    daftarProduk.scrollIntoView({
        behavior: "smooth"
    });

}


// ===============================
// FUNGSI PILIH PRODUK
// ===============================

function pilihProduk(namaKategori, namaProduk) {

    const produkDipilih = dataProduk[namaKategori].find(function(produk) {
        return produk.nama === namaProduk;
    });

    keranjangSiMUDA.push(produkDipilih);

    alert(namaProduk + " berhasil ditambahkan ke keranjang!");

    document.getElementById("daftarProduk").style.display = "none";

    tampilkanKeranjang();
}


// ===============================
// FUNGSI KEMBALI KE KATEGORI
// ===============================


function kembaliKeKategori() {

    // Menyembunyikan halaman produk
    document.getElementById("daftarProduk").style.display = "none";

    // Menyembunyikan halaman status
    document.getElementById("halamanStatus").style.display = "none";

    // Menampilkan kembali formulir pemesanan
    document.querySelector(".pesanan").style.display = "block";

    // Kembali ke bagian kategori
    document.querySelector(".kategori").scrollIntoView({
        behavior: "smooth"
    });

}

// ===============================
// FUNGSI MENAMPILKAN KERANJANG
// ===============================

function tampilkanKeranjang() {

    const halamanKeranjang = document.getElementById("halamanKeranjang");
    const isiKeranjang = document.getElementById("isiKeranjang");
    const totalKeranjang = document.getElementById("totalKeranjang");

    halamanKeranjang.style.display = "block";

    isiKeranjang.innerHTML = "";

    let total = 0;

    keranjangSiMUDA.forEach(function(produk, index) {

        const hargaAngka = Number(
            produk.harga.replace(/[^0-9]/g, "")
        );

        total += hargaAngka;

        isiKeranjang.innerHTML += `
            <div class="kartu-produk">
                <h3>${produk.nama}</h3>
                <p>Harga: ${produk.harga}</p>
                <button type="button" onclick="hapusDariKeranjang(${index})">
                    Hapus
                </button>
            </div>
        `;
    });

    totalKeranjang.textContent = "Total: Rp" + total.toLocaleString("id-ID");

    halamanKeranjang.scrollIntoView({
        behavior: "smooth"
    });
}
// ===============================
// FUNGSI HAPUS PRODUK DARI KERANJANG
// ===============================

function hapusDariKeranjang(index) {

    keranjangSiMUDA.splice(index, 1);

    tampilkanKeranjang();

}
function kembaliKeProduk() {

    document.getElementById("halamanKeranjang").style.display = "none";

    document.getElementById("daftarProduk").style.display = "block";

    document.getElementById("daftarProduk").scrollIntoView({
        behavior: "smooth"
    });

}


function lanjutKePemesanan() {

    if (keranjangSiMUDA.length === 0) {
        alert("Keranjang masih kosong.");
        return;
    }

    const daftarNama = keranjangSiMUDA.map(function(produk) {
        return produk.nama;
    }).join(", ");

    document.getElementById("detail").value = daftarNama;

    document.getElementById("halamanKeranjang").style.display = "none";

    document.querySelector(".pesanan").scrollIntoView({
        behavior: "smooth"
    });

}
// ===============================
// FUNGSI MEMBUKA PROFIL PENGGUNA
// ===============================

function bukaProfil() {

    if (akunSiMUDA === null) {
        alert("Silakan login terlebih dahulu.");
        return;
    }

    // Menampilkan data akun
    document.getElementById("profilNama").value = akunSiMUDA.nama;
    document.getElementById("profilTelepon").value = akunSiMUDA.telepon;
    document.getElementById("profilEmail").value = akunSiMUDA.email;

    // Menampilkan alamat yang sudah disimpan
    document.getElementById("profilAlamat").value = alamatProfilSiMUDA;

    // Menyembunyikan halaman lain
    document.querySelector(".welcome").style.display = "none";
    document.querySelector(".kategori").style.display = "none";
    document.getElementById("daftarProduk").style.display = "none";
    document.getElementById("halamanKeranjang").style.display = "none";
    document.getElementById("halamanStatus").style.display = "none";
    document.querySelector(".pesanan").style.display = "none";

    // Menampilkan halaman profil
    document.getElementById("halamanProfil").style.display = "block";

    document.getElementById("halamanProfil").scrollIntoView({
        behavior: "smooth"
    });
}
// ===============================
// FUNGSI MENYIMPAN PROFIL
// ===============================

function simpanProfil() {

    alamatProfilSiMUDA = document.getElementById("profilAlamat").value;

    alert("Profil berhasil disimpan!");

}
// ===============================

 // ===============================
 // FUNGSI KEMBALI DARI PROFIL
 // ===============================

function tutupProfil() {

    // Menyembunyikan halaman profil
    document.getElementById("halamanProfil").style.display = "none";

    // Menampilkan kembali beranda
    document.querySelector(".welcome").style.display = "block";
    document.querySelector(".kategori").style.display = "block";

    // Menampilkan kembali formulir pemesanan
    document.querySelector(".pesanan").style.display = "block";

    // Mengarahkan tampilan ke beranda
    document.querySelector(".welcome").scrollIntoView({
        behavior: "smooth"
    });

}
