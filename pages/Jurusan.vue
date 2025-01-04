<template>
  <div class="container">
    <div class="card mt-4">
      <div class="card-header bg-dark text-white text-center">
        <h4><i class="fas fa-graduation-cap"></i> Kompetensi Keahlian</h4>
      </div>
      <div class="card-body">
        <div class="row">
          <!-- Card 1 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/Tjkt.png" alt="TJKT" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">TJKT</h5>
                <p><strong>Sarana pendukung pembelajaran:</strong></p>
                <ul>
                  <li>Lab Komputer Modern</li>
                  <li>Server Virtual</li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Card 2 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/RPL.png" alt="RPL" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">RPL</h5>
                <p><strong>Sarana pendukung pembelajaran:</strong></p>
                <ul>
                  <li>Lab Coding</li>
                  <li>Perangkat Lunak Premium</li>
                </ul>
              </div>
            </div>
          </div>
          <!-- Card 3 -->
          <div class="col-md-6 col-lg-4 mb-4">
            <div class="card shadow-sm text-center">
              <div class="icon-wrapper mx-auto mt-3">
                <img src="/assets/image/TBSM.png" alt="TBSM" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">Teknik Otomotif</h5>
                <p><strong>Sarana pendukung pembelajaran:</strong></p>
                <ul>
                  <li>Lab Bengkel</li>
                  <li>Teknik Bisnis Sepedah Motor</li>
                </ul>
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
                <img src="/assets/image/DKV.png" alt="DKV" class="icon-img" />
              </div>
              <div class="card-body">
                <h5 class="card-title">DKV</h5>
                <p><strong>Sarana pendukung pembelajaran:</strong></p>
                <ul>
                  <li>Lab Praktek</li>
                  <li>Desain Kominikasi Visual</li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Tambahkan card lainnya sesuai kebutuhan -->
        </div>

        <!-- Footer Button -->
        <div class="footer">
          <NuxtLink to="/kompetensi/">
          <button class="btn btn-primary">Selengkapnya</button>
        </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  margin-top: 20px;
}

.card {
  border-radius: 10px;
  overflow: hidden;
}

.icon-wrapper {
  width: 60px;
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
