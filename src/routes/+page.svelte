<script >
    import WalletImage from "../components/WalletImage.svelte";
    import Content from "../components/Content.svelte";
    let selected
</script>
<div class="home-page__container flex  w-1/2 bg-white rounded-3xl overflow-hidden">
    <WalletImage selected = {selected} />
    <Content selected = {selected} />
</div>

