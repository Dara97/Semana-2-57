<template>
    <div>
        <div class="row mt-md-5 mt-sm-5 mt-xs-5">
            <div class="col-lg-6 col-xs-12" v-for="(movie,index) of movies" :key="index">
    <div class="d-flex justify-content-center align-items-center" >
    
                    <div class="p-3">
                        <img :src="movie.Poster" alt="Movie Poster">
                    </div>
                    
    
                    <div class="p-2">
                        <h3>{{movie.Title}}</h3>
                        <hr>
                        <p>
                            Año: {{movie.Year}}
                        </p>
                    </div>
    
     </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <a 
                    class="btn btn-outline-info"
                    :href="'https://www.imdb.com/title/' + movie.imdbID" 
                    target="_blank"
                    rel="noopener noreferrer"
                    > Pelicula
                    </a>
                </div>  
                 </div>  
    </div>    
</div>    
  

    
</template>
<script>
import axios from "axios";
export default {
  name: "SecNoticias",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=harry+potter&apikey=93ab8115")
      .then((response) => (this.movies = response.data.Search.slice(0, 4)));
  },
};
</script>
<style scoped>
</style>