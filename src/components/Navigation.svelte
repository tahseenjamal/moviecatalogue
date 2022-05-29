<script context='module'>
    import {writable} from 'svelte/store'
    export let title = writable('title');
</script>
<script>
    let inputValue = '';
    $title = '';
    function filterMovies(resp) {
        $title = resp;
    }
</script>

<div class="bg-gray-50 h-1/12 w-full shadow-lg py-4 mb-10">
    <nav class="flex mx-auto justify-between bg-gray-50 w-5/6">
        <p class="text-xl font-bold">The Movie DataBase</p>
        <div class="flex flex-row w-1/2 justify-end">
        <input type="text" name="" id="" placeholder="Name" bind:value="{inputValue}"
                class="pl-4 py-1 mx-4 w-2/4 border rounded-full">
        <button class="border border-blue-900 text-black text-base font-semibold
                        px-8 rounded-full hover:bg-blue-700 hover:text-white"
                on:click={filterMovies(inputValue)} >
            Search</button>
        </div>
    </nav>
</div>