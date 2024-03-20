<script setup>
const supabase = useSupabaseClient()
const books = ref([])

const getBooks = async () => {
  const {data, error } = await supabase.from('buku').select(`*, kategori(*)`)
  .like('judul', `%${keyword.value}%`)
  if(data) books.value = data
}

onMounted(() => {
  getBooks()
})

const keyword = ref('')

</script>

<template> 
<div class="container-fluid">
  <div class="row"> 
    <div class="col-lg-12"> 
      <h2 class="text-center my-4">PILIHAN BUKU</h2>
      <div class="my-3">
        <form @submit.prevent="getBooks">
          <input type="search" class="form-control rounded-3" placeholder="Mau baca apa hari ini?"> 
      </form>
      </div>
      <div class="my-3 text-muted">menampilkan 3 dari 3</div>
      <div class="row justify-content-between "> 
        <div v-for="(book,i) in books" :key="i" class="col-lg-2"> 
          <div class="card mb-3"> 
            <div class="card-body">
              <nuxt-link to="/rincian">
              <img src="~/assets/img/mtk.jpg" class="cover rounded-3" alt="cover 1">
            </nuxt-link>
            </div>
          </div>
        </div>
        <div v-for="(book,i) in books" :key="i" class="col-lg-2"> 
          <div class="card mb-3"> 
            <div class="card-body"> 
              <img src="~/assets/img/box.jpg" class="cover rounded-3" alt="cover 2">
      
            </div>
          </div>
        </div>
        <div v-for="(book,i) in books" :key="i" class="col-lg-2"> 
          <div class="card mb-3"> 
            <div class="card-body"> 
              <img src="~/assets/img/islam.png" class="cover rounded-3" alt="cover 3">
            </div>
          </div>
        </div>
        <nuxt-link to="/">
          <button type="submit" class="btn btn-warning btn-lg rounded-3 px-3">Kembali</button>
        </nuxt-link>
          
      </div>
    </div>
  </div>
</div>
</template>


<style scoped> 
.btn-warning{
  background-color: #2DEF34;
}
.card-body {
  width: 100%;
  height: 20em;
  padding: 0;
}
.cover {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 0 30;
}

input{
  background: #D9D9D9;
  height: 50px;
}
</style>