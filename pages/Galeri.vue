<template>
  <div class="container-fluid">
    <div class="col-lg-12">
          <h5 style="background-color: black;" class="text-white text-center rounded-3 p-2 m-3">
             <b>GALLERY SMKN 4 TASIKMALAYA</b>
          </h5>
        </div>

    <section class="gallery">
      <div class="gallery-item">
        <img src="/assets/image/PPLG.png" alt="PPLG" class="gallery-image" />
        <p class="gallery-caption"><b>RPS PPLG</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/Tkj.png" alt="TKJT" class="gallery-image" />
        <p class="gallery-caption"><b>RPS TJKT</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/DKVrg.png" alt="DKV" class="gallery-image" />
        <p class="gallery-caption"><b>>RPS DKV</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/Tsm.png" alt="TBSM" class="gallery-image" />
        <p class="gallery-caption"><b>Bengkel TBSM</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/Komite.png" alt="Ruangan Komite" class="gallery-image" />
        <p class="gallery-caption"><b>RUANGAN KOMITE</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/PERPUS.png" alt="Perpus" class="gallery-image" />
        <p class="gallery-caption"><b>PERPUSTAKAAN</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/AULA.png" alt="AULA" class="gallery-image" />
        <p class="gallery-caption"><b>SMKN 4 Tasikmalaya</b></p>
      </div>
      <div class="gallery-item">
        <img src="/assets/image/SENI.png" alt="seni" class="gallery-image" />
        <p class="gallery-caption"><b>RUANG SENI</b></p>
      </div>
    </section>

    <footer class="footer">
      <p>&copy; 2024 SMK Unggul. Semua hak dilindungi.</p>
    </footer>
  </div>
</template>

<style scoped>

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
  margin: 20px 0;
}

.gallery-item {
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 10px;
  transition: transform 0.3s;
}

.gallery-item:hover {
  transform: scale(1.05);
}

.gallery-image {
  max-width: 100%;
  border-radius: 8px;
}

.gallery-caption {
  color: #555;
  margin-top: 10px;
}

.footer {
  margin-top: 20px;
  font-size: 0.9em;
  color: #555;
}
</style>
