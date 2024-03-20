<template>
  <div class="container-fluid p-2 mt-3">
    <div class="row mt-4">
      <div class="col-4 justify-content-center">
        <img src="~/assets/img/mtk.jpg" class="cover rounded-4" alt="cover 1" width="240px" height="340px">
      </div>
      <div class="col-8">
        <h2> Rincian Buku</h2>
        <p> Penerbit: Pusat kurikulum dan pembukuan</p>
        <p> ISBN    : 978-602-244-788-7</p>
        <p> Penulis  : Dicky Susanto, Savitri K.</p>
        <p> Tahun terbit : 2021</p>
        <p class="mt-5"> Buku ini disiapkan oleh Pemerintah dalam rangka pemenuhan kebutuhan buku pendidikan yang 
        bermutu, murah, dan merata sesuai dengan amanat dalam UU No. 3 Tahun 2017. 
        Buku ini digunakan secara terbatas pada Sekolah Penggerak. 
        Buku ini disusun dan ditelaah oleh berbagai pihak di bawah koordinasi Kementerian Pendidikan, Kebudayaan, Riset dan Teknologi. Buku ini merupakan dokumen hidup yang senantiasa diperbaiki, diperbaharui, 
        dan dimutakhirkan sesuai dengan dinamika kebutuhan dan perubahan zaman. 
        Masukan dari berbagai kalangan yang dialamatkan kepada penulis atau melalui alamat surel buku@kemdikbud.go.id diharapkan dapat meningkatkan kualitas buku ini.</p>
      </div>
    </div>
    <nuxt-link to="/buku/">
          <button type="submit" class="btn btn-warning btn-lg rounded-3 px-3">Kembali</button>
        </nuxt-link>
    </div>
</template>

<style scoped>
.btn-warning{
  background-color: #2DEF34;
}
</style>
