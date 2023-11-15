<script>
    import {selectedStore} from "$lib/store.js";

    let selected;

    selectedStore.subscribe(value => {
        selected = value;
    });
</script>
<div class=" home-page__image-box w-2/6 ">
    <img src="/{selected}.png" alt="{selected}" class="w-full h-full"/>
</div>