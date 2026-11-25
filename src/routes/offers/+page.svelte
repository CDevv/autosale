<script lang="ts">
    import Heading from "#lib/Heading.svelte";
    import OfferCard from "#lib/OfferCard.svelte";
    import SearchForm from "#lib/SearchForm.svelte";

    let searchEnabled = $state(false);

    function toggleSearch() {
        searchEnabled = !searchEnabled;
    }
</script>

<svelte:head>
    <title>Autosale.bg - Обяви</title>
</svelte:head>

<div class="flex flex-row gap-2">
    <Heading title="Последни обяви" />
    <button class="button max-w-3xs min-w-2xs" onclick={toggleSearch}>
        Търсене
    </button>
    <a href="/newoffer" class="button max-w-3xs min-w-2xs text-center">
        Пусни обява
    </a>
</div>

<br />
<SearchForm hidden={!searchEnabled} />
<div class="grid grid-cols-2 grid-rows-1">
    <OfferCard />
</div>
