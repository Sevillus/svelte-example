<script>

    // Logika aktualizacji wartości sklepu
    import {selectedStore} from "$lib/store.js";
    import {colors} from "../constants/colors.js";

    function updateSelected(value) {
        selectedStore.set(value);
    }
    let selected ;
    selectedStore.subscribe(num => {
        selected = num
    })
</script>
<p class="mt-2 mb-2 font-semibold">Color</p>
<div  class="flex gap-6 ">

    {#each colors as color}
        <button
                on:click={() => updateSelected(color.index)}
                class=""
        >
            <div  class="w-10 h-10 rounded-full border-black" class:border-2 = {selected === color.index} style="background-color: {color.color}">
            </div>
        </button>
    {/each}
</div>