<script>
  export default {
    data() {
      return {
        data_images: [
          {
            id: 1,
            logo_name: "ENGLAND",
            logo_file: "England.png",
            palyed: 5,
            scores: 3,
            lose: 0,
            rating: 5,
          },
          {
            id: 2,
            logo_name: "LIVERPOOL",
            logo_file: "Liverpool.png",
            palyed: 6,
            scores: 2,
            lose: 2,
            rating: 3,
          },
          {
            id: 3,
            logo_name: "PERSIB",
            logo_file: "Persib.png",
            palyed: 5,
            scores: 2,
            lose: 2,
            rating: 4,
          },
          {
            id: 4,
            logo_name: "PORTUGAL",
            logo_file: "Portugal.png",
            palyed: 7,
            scores: 2,
            lose: 3,
            rating: 3,
          },
          {
            id: 5,
            logo_name: "VALENCIA",
            logo_file: "Valencia.png",
            palyed: 5,
            scores: 2,
            lose: 2,
            rating: 3,
          },
          {
            id: 6,
            logo_name: "KFA",
            logo_file: "Kfa.png",
            palyed: 5,
            scores: 2,
            lose: 3,
            rating: 4,
          },
         
        ],
      };
    },
  };
</script>
<template>
  <div>
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <div v-for="data_images in data_images" class="col">
        <a class="btn btn-link btn-block">
          <router-link :to="'/detail/' + data_images.id">
            <div class="col">
              <div class="card h-100">
                <div class="card-body">
                  <img
                    :src="'/src/assets/logo_bola/' + data_images.logo_file"
                    class="card-img-top"
                    alt="404"
                  />
                </div>
                <h5 id="text__decotation" class="text-center">
                  {{ data_images.logo_name }}
                </h5>
              </div>
            </div>
          </router-link>
        </a>
      </div>
    </div>
  </div>
</template>

<style>
  img {
    width: 100px;
    height: 150px;
  }
</style>
