<script>
    import EmailInfo from "#lib/EmailInfo.svelte";
    import Heading from "#lib/Heading.svelte";
    import OfferCard from "#lib/OfferCard.svelte";
    import TelephoneInfo from "#lib/TelephoneInfo.svelte";
</script>

<div class="max-w-[1450px] mx-auto px-4 md:px-6 py-8">
    <!-- горна част -->
    <div class="mb-7">
        <a
            href="/dealers"
            class="inline-flex items-center gap-2 text-slate-600 hover:text-orange-600 font-semibold mb-5 transition-colors"
        >
            <span class="text-xl">←</span>
            Обратно към дилърите
        </a>

        <Heading title="Ивайло" />
    </div>

    <!-- информация -->
    <div class="lg:col-span-1 mb-7">
        <div
            class="bg-white border border-gray-100 rounded-3xl shadow-xl overflow-hidden p-6 md:p-7"
        >
            <div class="flex flex-row gap-5">
                <TelephoneInfo />
                <EmailInfo />
            </div>
        </div>
    </div>

    <!-- обяви -->
    <div class="mb-7">
        <Heading title="Обяви" />
    </div>

    <div class="grid grid-cols-2 grid-rows-1">
        <OfferCard />
    </div>
</div>
