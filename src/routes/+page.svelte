
<script lang="ts">
    import Banner from "#lib/Banner.svelte";
    import OfferCard from "#lib/OfferCard.svelte";
</script>

<div class="max-w-[1550px] mx-auto px-4 md:px-6 py-5">

    <!-- Голям банер -->
    <Banner />

    <!-- Полезни линкове -->
    <section class="bg-white rounded-2xl shadow-xl border border-gray-100 px-6 py-5 md:px-9 md:py-6 mb-8">

        <!-- Заглавие -->
        <h2 class="flex items-center gap-4 text-2xl md:text-3xl font-bold text-slate-900 mb-4">

            <!-- Икона за линк -->
            <svg
                class="w-9 h-9 text-orange-500 shrink-0"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="3"
                stroke-linecap="round"
                stroke-linejoin="round"
            >
                <path d="M10 13a5 5 0 0 0 7.1 0l3-3a5 5 0 0 0-7.1-7.1l-1.7 1.7" />
                <path d="M14 11a5 5 0 0 0-7.1 0l-3 3a5 5 0 0 0 7.1 7.1l1.7-1.7" />
            </svg>

            Полезни линкове
        </h2>

        <!-- Двата бутона -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-5 md:gap-8">

            <!-- Проверка на автомобил -->
            <a
                href="https://public-eis.rta.government.bg/public-vehicle-check/vin-check"
                target="_blank"
                rel="noopener noreferrer"
                class="group flex items-center justify-between gap-4 bg-white rounded-full border border-gray-100 shadow-md hover:shadow-xl hover:border-orange-200 px-6 py-4 transition-all duration-300"
            >
                <div class="flex items-center gap-5">

                    <!-- Щит -->
                    <svg
                        class="w-9 h-9 text-orange-500 shrink-0"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10Z" />
                        <path d="m9 12 2 2 4-4" />
                    </svg>

                    <span class="text-base md:text-lg font-bold text-slate-900">
                        Информационна система за проверка
                    </span>
                </div>

                <span class="text-orange-500 text-3xl group-hover:translate-x-1 transition-transform">
                    →
                </span>
            </a>

            <!-- Авточасти -->
            <a
                href="https://sova.bg/category/EDbgyUs1"
                target="_blank"
                rel="noopener noreferrer"
                class="group flex items-center justify-between gap-4 bg-white rounded-full border border-gray-100 shadow-md hover:shadow-xl hover:border-orange-200 px-6 py-4 transition-all duration-300"
            >
                <div class="flex items-center gap-5">

                    <!-- Зъбно колело -->
                    <svg
                        class="w-9 h-9 text-orange-500 shrink-0"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <circle cx="12" cy="12" r="3" />
                        <path d="M19.4 15a1.7 1.7 0 0 0 .34 1.88l.06.06-2.8 2.8-.06-.06A1.7 1.7 0 0 0 15 19.4a1.7 1.7 0 0 0-1 1.56V21h-4v-.04A1.7 1.7 0 0 0 9 19.4a1.7 1.7 0 0 0-1.88.34l-.06.06-2.8-2.8.06-.06A1.7 1.7 0 0 0 4.6 15a1.7 1.7 0 0 0-1.56-1H3v-4h.04A1.7 1.7 0 0 0 4.6 9a1.7 1.7 0 0 0-.34-1.88L4.2 7.06l2.8-2.8.06.06A1.7 1.7 0 0 0 9 4.6a1.7 1.7 0 0 0 1-1.56V3h4v.04A1.7 1.7 0 0 0 15 4.6a1.7 1.7 0 0 0 1.88-.34l.06-.06 2.8 2.8-.06.06A1.7 1.7 0 0 0 19.4 9a1.7 1.7 0 0 0 1.56 1H21v4h-.04A1.7 1.7 0 0 0 19.4 15Z" />
                    </svg>

                    <span class="text-base md:text-lg font-bold text-slate-900">
                        Търсене на производители на части в Sova.bg
                    </span>
                </div>

                <span class="text-orange-500 text-3xl group-hover:translate-x-1 transition-transform">
                    →
                </span>
            </a>

        </div>
    </section>

    <!-- Последни обяви -->
    <section class="mb-10">

        <h2 class="text-2xl md:text-3xl font-bold text-gray-900 mb-5 flex items-center gap-4">
            <span class="w-1.5 h-9 bg-orange-600 rounded-full"></span>
            Последни обяви
        </h2>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
            <OfferCard />
        </div>

    </section>

</div>
