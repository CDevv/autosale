<script>
    import Banner from "#lib/Banner.svelte";
    import OfferCard from "#lib/OfferCard.svelte";
</script>

<Banner />
<br />
<div class="card">
    <h2 class="text-3xl">Полезни линкове</h2>
    <div class="grid grid-cols-2 gap-1">
        <a
            target="_blank"
            class="button text-2xl"
            href="https://public-eis.rta.government.bg/public-vehicle-check/vin-check"
            >Информационна система за проверка</a
        >
        <a
            target="_blank"
            class="button text-2xl"
            href="https://sova.bg/category/EDbgyUs1"
            >Търсене на производители на части в Sova.bg</a
        >
    </div>
</div>
<br />
<div>
    <h1 class="text-3xl">Последни обяви</h1>
    <br />
    <div class="grid grid-cols-3">
        <OfferCard />
    </div>
</div>
