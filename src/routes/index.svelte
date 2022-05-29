<script context='module'>
  export async function load({ fetch }) {
    const res = await fetch(
      'https://api.themoviedb.org/3/movie/popular?api_key=c6b27a7dcdfff875b7054be27d1ef84e&page=1'
    );
    const data = await res.json();
    if (res.ok) {
      return { 
        props : { movieInfo: data.results} 
      };
    }
  }
</script>

<script>
  import Navigation from "../components/Navigation.svelte";
  import PopularMovies from "../components/PopularMovies.svelte";
  export let movieInfo;
</script>

<div class="flex flex-col">
 
  <Navigation/>

  <div class='justify-center'>
    <PopularMovies {movieInfo}/>
  </div>

</div>
