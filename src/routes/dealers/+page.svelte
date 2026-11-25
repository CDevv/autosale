<script lang="ts">
    import DealerCard from "#lib/DealerCard.svelte";

    let search = $state("");

    let showDealer = $derived(
        "Ивайло"
            .toLocaleLowerCase("bg-BG")
            .includes(search.trim().toLocaleLowerCase("bg-BG")),
    );
</script>

<svelte:head>
    <title>Autosale.bg - Дилъри</title>
</svelte:head>

<!-- ГОЛЯМ БАНЕР -->
<section
    class="relative min-h-[300px] md:min-h-[340px] rounded-3xl overflow-hidden shadow-2xl bg-slate-950 mb-6"
>
    <!-- Тъмен градиент -->
    <div
        class="absolute inset-0 bg-gradient-to-r from-slate-950 via-slate-950/90 to-slate-950/20"
    ></div>

    <!-- Оранжева декорация -->
    <div
        class="absolute top-0 left-0 w-2 h-full bg-gradient-to-b from-orange-400 to-orange-600"
    ></div>

    <!-- Текст -->
    <!-- Текст -->
    <div
        class="relative z-10 min-h-[300px] md:min-h-[340px] flex flex-col justify-center px-8 md:px-14 py-10"
    >
        <h1 class="text-4xl md:text-6xl font-bold text-white mb-4">
            Нашите <span class="text-orange-500">дилъри</span>
        </h1>

        <p class="text-lg md:text-xl text-gray-200 max-w-xl mb-7">
            Разгледайте автомобилните дилъри в платформата и открийте техните
            предложения на едно място.
        </p>

        <!-- Предимства -->
        <div class="flex flex-wrap gap-3">
            <span
                class="flex items-center gap-2 bg-white/10 border border-white/20 text-white text-sm md:text-base px-4 py-2 rounded-full backdrop-blur-sm"
            >
                <span class="text-orange-400">✓</span>
                Автомобилни дилъри
            </span>

            <span
                class="flex items-center gap-2 bg-white/10 border border-white/20 text-white text-sm md:text-base px-4 py-2 rounded-full backdrop-blur-sm"
            >
                <span class="text-orange-400">✓</span>
                Разнообразни предложения
            </span>

            <span
                class="flex items-center gap-2 bg-white/10 border border-white/20 text-white text-sm md:text-base px-4 py-2 rounded-full backdrop-blur-sm"
            >
                <span class="text-orange-400">✓</span>
                Лесно разглеждане
            </span>
        </div>
    </div>
</section>

<!-- ТЪРСЕНЕ НА ДИЛЪР -->
<section
    class="bg-white rounded-2xl shadow-xl border border-gray-100 p-5 md:p-7 mb-10"
>
    <div class="flex items-center gap-3 mb-5">
        <span class="w-1.5 h-8 bg-orange-600 rounded-full"></span>

        <h2 class="text-2xl font-bold text-slate-900">Намери дилър</h2>
    </div>

    <div class="relative">
        <!-- Икона -->
        <svg
            class="absolute left-5 top-1/2 -translate-y-1/2 w-6 h-6 text-orange-500"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
        >
            <circle cx="11" cy="11" r="8" />
            <path d="m21 21-4.35-4.35" />
        </svg>

        <input
            type="search"
            bind:value={search}
            placeholder="Търси дилър по име..."
            aria-label="Търси дилър по име"
            class="w-full bg-gray-50 border-2 border-gray-200 focus:border-orange-500 focus:outline-none rounded-2xl py-4 pl-14 pr-5 text-lg text-gray-900 placeholder:text-gray-400 transition-colors"
        />
    </div>
</section>

<!-- СПИСЪК С ДИЛЪРИ -->
<section class="mb-12">
    <!-- Заглавие -->
    <div class="flex flex-wrap items-center justify-between gap-4 mb-6">
        <h2
            class="flex items-center gap-4 text-2xl md:text-3xl font-bold text-slate-900"
        >
            <span class="w-1.5 h-9 bg-orange-600 rounded-full"></span>
            Регистрирани дилъри
        </h2>

        <span
            class="bg-orange-100 text-orange-700 font-semibold px-4 py-2 rounded-full"
        >
            Разгледай предложенията
        </span>
    </div>

    <!-- Карти -->
    {#if showDealer}
        <div
            class="bg-white rounded-3xl shadow-xl border border-gray-100 p-4 md:p-6"
        >
            <div class="flex items-center gap-4 mb-5">
                <!-- Лого -->
                <div
                    class="w-16 h-16 md:w-20 md:h-20 shrink-0 rounded-2xl bg-slate-950 flex items-center justify-center shadow-md"
                >
                    <span class="text-white text-sm md:text-base font-bold">
                        <span class="text-orange-500">auto</span>sale.bg
                    </span>
                </div>

                <!-- Информация -->
                <div>
                    <h3 class="text-2xl font-bold text-slate-900 mb-1">
                        Автомобилен дилър
                    </h3>

                    <p class="text-gray-500">
                        Разгледайте наличните предложения
                    </p>
                </div>
            </div>

            <!-- Твоят съществуващ компонент -->
            <div class="[&_.card]:rounded-2xl [&_.card]:border-gray-100">
                <DealerCard />
            </div>
        </div>
    {:else}
        <div class="bg-white rounded-2xl shadow-md p-10 text-center">
            <p class="text-xl font-semibold text-gray-700">
                Няма намерен дилър с това име.
            </p>

            <p class="text-gray-500 mt-2">Опитайте с друго име.</p>
        </div>
    {/if}
</section>
