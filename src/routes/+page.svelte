<script>
    import Banner from "#lib/Banner.svelte";
    import OfferCard from "#lib/OfferCard.svelte";
</script>

<br />
<Banner />
<br />
<div>
    <h1 class="text-3xl">Последни обяви</h1>
    <br />
    <div class="grid grid-cols-3 grid-rows-1">
        <OfferCard />
    </div>
</div>
