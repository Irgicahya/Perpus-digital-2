<template> 
<div class="container-fluid"> 
  <div class="row my-5">
    <div class="col-lg-6">
      <nuxt-link to="/pengunjung/tambah">
        <div class="card bg-pengunjung rounded-5 m-3">
          <div class="card-body">
            <h2> Pengunjung </h2>
          </div>
        </div>
      </nuxt-link>
    </div>
    <div class="col-lg-6"> 
      <nuxt-link to="/buku"> 
        <div class="card bg-buku rounded-5 m-3"> 
          <div class="card-body"> 
            <h2> Cari Buku </h2>
          </div>
        </div>
      </nuxt-link>
    </div>
  </div>
</div>
<h1 style="margin: 25px;"> <strong> STATISTIK</strong> </h1>
<div class="container-fluid">
  <div class="row justify-content-evenly rounded-5">
    <div class="col-5">
      <div class="jeep">
        <h1> 7 Pengunjung </h1>
      </div>
    </div>
    <div class="col-5">
      <div class="raccing2">
        <h1> 3 Buku </h1>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped> 
.card {
  height: 250px;
  box-shadow: 1px 1px 10px #424242;
}
.card.bg-pengunjung {
  background-image: url('../assets/img/bg-home-kunjungan.jpeg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.card.bg-buku {
  background: url('../assets/img/bg-home-cari-buku.jpg')no-repeat center center;
  background-size: cover;
}

.jeep{
  height: 200px;
  box-shadow: 1px 1px 10px;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgb(242, 255, 167);
}
  .raccing2{
    height: 200px;
    box-shadow: 1px 1px 10px;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgb(101, 250, 200);


  }

</style> 