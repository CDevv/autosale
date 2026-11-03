<script lang="ts">
    import OfferCard from "#lib/OfferCard.svelte";
    import SearchForm from "#lib/SearchForm.svelte";

    let searchEnabled = $state(false);

    function toggleSearch() {
        searchEnabled = !searchEnabled;
    }
</script>

<br />
<div class="flex flex-row gap-2">
    <h1 class="text-3xl mt-0.5 mb-0.5 grow">Последни оферти</h1>
    <button class="button max-w-3xs min-w-2xs" onclick={toggleSearch}
        >Търсене</button
    >
</div>

<br />
<SearchForm hidden={!searchEnabled} />
<div class="grid grid-cols-3 grid-rows-1">
    <OfferCard />
</div>
