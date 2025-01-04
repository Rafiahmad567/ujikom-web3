<template>
  <div id="app">
    <div class="row">
      <!-- Slider Berita -->
      <div class="col-lg-9">
        <div class="slider-content">
          <img src="/assets/image/logo (1).png" alt="Berita" class="slider-image" />
          </div>
        </div>

      <!-- Sambutan Kepala Sekolah -->
      <div class="sambutan">
        <h3>Sambutan Kepala Sekolah</h3>
        <div class="sambutan-content">
          <img src="/assets/image/skyyy.png" alt="Kepala Sekolah" class="kepsek-image" />
          <marquee direction="up" scrollamount="2" class="marquee-text">
            Assalamu'alaikum Wr, Wb<br /><br />
            Segala puji dan syukur kita panjatkan kehadirat Alloh SWT,
             semoga kita semua ada dalam lindungan-Nya dan atas perkenan-Nya pula kami
              dapat menghadirkan web site SMK Negeri 4 Tasikmalaya ini
          </marquee>
        </div>
      </div>
      <div class="row">
      <!-- Index Berita -->
      <div class="col-md-8">
        <div class="card">
          <div class="card-header bg-primary text-white text-center">
            <strong>Index Berita</strong>
          </div>
          <div class="card-body">
            <div v-for="(news, index) in indexBerita" :key="index" class="mb-3 border-bottom pb-2">
              <h5><a :href="news.link" class="text-dark">{{ news.title }}</a></h5>
              <small class="text-muted">{{ news.date }} - {{ news.author }}</small>
            </div>
            <button class="btn btn-primary btn-sm" @click="loadMore">Selanjutnya</button>
          </div>
        </div>
      </div>

      <!-- Berita Pilihan -->
      <div class="col-md-4">
        <div class="card">
          <div class="card-header bg-success text-white text-center">
            <strong>Berita Pilihan</strong>
          </div>
          <div class="card-body">
            <div v-for="(news, index) in beritaPilihan" :key="index" class="mb-3 border-bottom pb-2">
              <h5><a :href="news.link" class="text-dark">{{ news.title }}</a></h5>
              <small class="text-muted">{{ news.date }} - {{ news.author }}</small>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="content bg-secondary">
      <div class="col-lg-12">
          <h5 style="background-color: Secondary;" class="text-white text-center rounded-3 p-2 m-3">
             <b>STATISTIK</b>
          </h5>
        </div>
      <div class="stats-grid">
        <div class="stat-item bg-success">
          <h3>Jumlah Siswa</h3>
          <p class="value">1116</p>
        </div>
        <div class="stat-item bg-primary">
          <h3>Jumlah Rombel</h3>
          <p class="value">34</p>
        </div>
        <div class="stat-item bg-danger">
          <h3>Jumlah Guru</h3>
          <p class="value">60</p>
        </div>
        <div class="stat-item bg-warning">
          <h3>Jumlah Tenaga Administrasi</h3>
          <p class="value">12</p>
        </div>
      </div>
      </div>
    </div>
    <div class="card-header bg-dark text-white text-center">
        <h4><i class="fas fa-graduation-cap"></i> Gallery Smkn 4 Tasikmalaya</h4>
      </div>
      <div class="card-body">
        <div class="row">
          <!-- Card 1 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/PPLG.png" alt="TJKT" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">PPLG</h5>
                <p><strong>Ruangan praktik PPLG</strong></p>
              </div>
            </div>
          </div>

          <!-- Card 2 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/TKJ.png" alt="TJKT" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">TJKT</h5>
                <p><strong>Ruangan Praktik TJKT</strong></p>
              </div>
            </div>
          </div>
          <!-- Card 3 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/tsm.png" alt="TBSM" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">TBSM</h5>
                <p><strong>Ruangan Pembelajaran TBSM</strong></p>
              </div>
            </div>
          </div>
          <!-- Card 4 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/TOI.png" alt="TOI" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">TOI</h5>
                <p><strong>Sarana pendukung pembelajaran:</strong></p>
                <ul>
                  <li>Lab Praktek</li>
                  <li>Teknik Otomasi Industri</li>
                </ul>
              </div>
            </div>
          </div>
          <!-- Card 5 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/DKVrg.png" alt="DKV" class="icon-img" width="80%" />
              </div>
              <div class="card-body">
                <h5 class="card-title">DKV</h5>
                <p><strong>Ruangan Praktik DKV</strong></p>
              </div>
              </div>
            </div>
          </div>
          <div class="footer pb-3">
          <NuxtLink to="/Galeri/">
          <button class="btn btn-primary">Selengkapnya</button>
        </NuxtLink>
        </div>
        </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      indexBerita: [
        {
          title: "Pengumuman Kelulusan Siswa Tahun Pelajaran 2023/2024",
          date: "06-05-2024",
          author: "SMKN 4 Tasikmalaya",
          link:"https://www.smkn4-tsm.sch.id/#lg=1&slide=0" 
        },
        {
          title: "Hasil Seleksi PPDB Tahap 2 Tahun 2020",
          date: "08-07-2020",
          author: "Taufik Hidayat",
          link: "#",
        },
        {
          title: "Daftar Ulang PPDB SMKN 4 Tasikmalaya Tahap 1 Tahun 2020",
          date: "23-06-2020",
          author: "Muhammad Hilmi Ahadiat",
          link: "#",
        },
      ],
      beritaPilihan: [
        {
          title: "Pengumuman Kelulusan Siswa Tahun Pelajaran 2021/2022",
          date: "03-06-2022",
          author: "SMKN 4 Tasikmalaya",
          link: "#",
        },
        {
          title: "Daftar Ulang PPDB SMKN 4 Tasikmalaya Tahap 1 Tahun 2020",
          date: "23-06-2020",
          author: "Muhammad Hilmi Ahadiat",
          link: "#",
        },
        {
          title: "Penerimaan Peserta Didik Baru 2020",
          date: "02-03-2020",
          author: "Aceng Saripudin",
          link: "#",
        },
        // {
        //   title: "Kunjungan Industri Kelas XI Tahun 2020",
        //   date: "19-02-2020",
        //   author: "SMKN 4 Tasikmalaya",
        //   link: "#",
        // },
      ],
    };
  },
  methods: {
    loadMore() {
      alert("Load more news clicked!");
    },
  },
};
</script>

<style scoped>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
}

.container {
  display: flex;
  gap: 20px;
  padding: 20px;
}

/* Slider */
.slider {
  flex: 3;
  position: relative;
  background-color: #fff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
}

.slider-content {
  padding: 5px;
  text-align: center;
}

.slider-content h2 {
  font-size: 18px;
  background-color: rgba(0, 0, 0, 0.7);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}

.slider-content p {
  margin: 10px 0;
  font-size: 14px;
  color: #0c0a0a;
}

.slider-image {
  width: 100%;
  height: auto;
  margin: 10px 0;
}

.slider-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-berita {
  background-color: #070809;
  color: #fff;
  padding: 8px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn-berita:hover {
  background-color: #0056b3;
}

.tanggal {
  font-size: 12px;
  color: #888;
}

.slider-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  border: none;
  border-radius: 50%;
  padding: 10px;
  cursor: pointer;
  font-size: 16px;
}

.slider-btn-left {
  left: 10px;
}

.slider-btn-right {
  right: 10px;
}

/* Sambutan Kepala Sekolah */
.sambutan {
  flex: 1;
  background-color: #fff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
  text-align: center;
}

.sambutan h3 {
  background-color: #04821d;
  color: #fff;
  padding: 10px;
  margin: 0;
}

.sambutan-content {
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.kepsek-image {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-bottom: 10px;
}

.marquee-text {
  width: 100%;
  font-size: 14px;
  color: #555;
}

.statistik-data {
  font-family: Arial, sans-serif;
  margin: 20px;
}

.breadcrumb {
  font-size: 14px;
  color: gray;
  margin-bottom: 20px;
}

.content {
  background-color: #f9f9f9;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.stat-item {
  /* background-color: #bfebfe; */
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.stat-item h3 {
  margin-bottom: 10px;
}

.stat-item .value {
  font-size: 24px;
  font-weight: bold;
}

.container {
  margin-top: 20px;
}

.card {
  border-radius: 10px;
  overflow: hidden;
}

.icon-wrapper {
  width: 60%;
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.card-title {
  font-weight: bold;
  font-size: 1.2rem;
  margin-top: 10px;
}

ul {
  padding-left: 1rem;
}

ul li {
  list-style: disc;
}

.footer {
  text-align: center;
  margin-top: 20px;
}

.footer .btn {
  background-color: rgb(51, 178, 242);
  color: black;
}
</style>
