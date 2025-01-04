<template>
  <div id="app" class="container">
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
          link: "#"
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
         {
           title: "Kunjungan Industri Kelas XI Tahun 2020",
           date: "19-02-2020",
          author: "SMKN 4 Tasikmalaya",
          link: "#",
         },
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

<style>
.container {
  margin-top: 20px;
}

.card {
  margin-bottom: 20px;
}

a {
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>
