<script>
    export let movie;
</script>


<div class="relative flex flex-col h-full m-4 w-1/6 
            rounded-md hover:border hover:border-gray-50 duration-100 cursor-pointer">
    
    <div class="absolute -inset-0.5 bg-gray-900 rounded-md opacity-100 blur-md"></div>

    <div class="relative bg-white rounded-md overflow-hidden">
        <div class="m-1 rounded-md overflow-hidden">
            <img src="{'https://image.tmdb.org/t/p/w440_and_h660_face' + movie.backdrop_path}" alt="">
        </div>
        <div class="px-4 py-2">
            <p class="text-sm font-bold truncate pb-2">{movie.title}</p>
            <p class="text-xs font-light">{movie.release_date}</p>
        </div>
    </div>
</div>


