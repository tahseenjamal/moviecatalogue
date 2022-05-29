<script>
    import { Result } from "postcss";
    import { each } from "svelte/internal"
    import MovieCards from "./MovieCards.svelte";
    import { title } from "./Navigation.svelte";
    export let movieInfo = "";

    function filter(query, data) {
        return query.toLowerCase().match(data.toLowerCase());
    }
</script>

<div class="flex flex-wrap justify-center">
    {#each movieInfo as movie}
        {#if filter(movie.title, $title)}
            <MovieCards {movie} />
        {:else if $title == ''}
            <MovieCards {movie} />
        {/if}
    {/each}
</div>