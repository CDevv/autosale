
<script lang="ts">
    import image from "#lib/assets/21764003891272177_bw.webp";

    const characteristics = [
        { icon: "📅", name: "Година", value: "2019" },
        { icon: "🛣️", name: "Пробег", value: "85 000 км" },
        { icon: "⛽", name: "Гориво", value: "Дизел" },
        { icon: "⚙️", name: "Скорости", value: "Автоматик" },
        { icon: "⚡", name: "Мощност", value: "240 к.с." },
        { icon: "🚙", name: "Задвижване", value: "4×4" }
    ];
</script>

<div class="max-w-[1450px] mx-auto px-4 md:px-6 py-8">

    <!-- ГОРНА ЧАСТ -->
    <div class="mb-7">

        <a
            href="/offers"
            class="inline-flex items-center gap-2 text-slate-600 hover:text-orange-600 font-semibold mb-5 transition-colors"
        >
            <span class="text-xl">←</span>
            Обратно към обявите
        </a>

        <div class="flex flex-wrap items-center justify-between gap-4">

            <div>
                <div class="flex items-center gap-3 mb-2">
                    <span class="w-1.5 h-10 rounded-full bg-orange-600"></span>

                    <h1 class="text-3xl md:text-4xl font-black text-slate-950">
                        Име на обява
                    </h1>
                </div>

                <p class="text-gray-500 text-lg ml-5">
                    Range Rover Velar • 2019 г.
                </p>
            </div>

            <div class="bg-white border border-gray-200 rounded-full shadow-sm px-5 py-3">
                <span class="text-sm font-semibold text-gray-500">
                    📅 18.11.2026 г.
                </span>
            </div>

        </div>

    </div>

    <!-- СНИМКА И ПРОДАВАЧ -->
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-8">

        <!-- ЛЯВА ЧАСТ -->
        <div class="lg:col-span-2">

            <div class="bg-white border border-gray-100 rounded-3xl shadow-xl overflow-hidden">

                <!-- СНИМКА -->
                <div class="relative bg-slate-100 p-4 md:p-6">

                    <img
                        src={image}
                        alt="Range Rover Velar"
                        class="w-full h-[280px] sm:h-[400px] lg:h-[480px] object-contain rounded-2xl"
                    />

                    <div class="absolute bottom-8 right-8 bg-slate-900/85 text-white rounded-full px-4 py-2 text-sm font-semibold">
                        1 снимка
                    </div>

                </div>

                <!-- ХАРАКТЕРИСТИКИ -->
                <div class="p-6 md:p-8">

                    <div class="flex items-center gap-3 mb-6">

                        <div class="w-1.5 h-8 bg-orange-600 rounded-full"></div>

                        <h2 class="text-2xl md:text-3xl font-bold text-slate-900">
                            Характеристики
                        </h2>

                    </div>

                    <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                        {#each characteristics as item (item.name)}

                            <div class="flex items-center gap-3 rounded-2xl bg-slate-50 border border-gray-100 p-4 hover:border-orange-200 hover:shadow-md transition-all">

                                <div class="w-11 h-11 shrink-0 flex items-center justify-center rounded-xl bg-orange-100 text-xl">
                                    {item.icon}
                                </div>

                                <div class="min-w-0">

                                    <p class="text-sm text-gray-500 mb-1">
                                        {item.name}
                                    </p>

                                    <p class="text-base md:text-lg font-bold text-slate-900">
                                        {item.value}
                                    </p>

                                </div>

                            </div>

                        {/each}

                    </div>

                </div>

            </div>

        </div>

        <!-- ДЯСНА ЧАСТ -->
        <div class="lg:col-span-1">

            <div class="bg-white border border-gray-100 rounded-3xl shadow-xl overflow-hidden">

                <!-- ЦЕНА -->
                <div class="bg-gradient-to-br from-orange-50 to-white p-7 border-b border-orange-100">

                    <p class="text-lg font-semibold text-gray-500 mb-2">
                        Цена
                    </p>

                    <p class="text-5xl md:text-6xl font-black text-orange-600">
                        €50
                    </p>

                </div>

                <!-- БУТОН -->
                <div class="px-6 pt-6">

                    <a
                        href="/"
                        class="flex items-center justify-center gap-3 w-full bg-gradient-to-r from-orange-600 to-orange-500 hover:from-orange-500 hover:to-orange-400 text-white text-lg font-bold py-4 px-5 rounded-2xl shadow-lg shadow-orange-500/20 transition-all"
                    >

                        <svg
                            class="w-6 h-6"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <rect x="3" y="5" width="18" height="14" rx="2" />
                            <path d="m3 7 9 6 9-6" />
                        </svg>

                        Изпрати запитване

                    </a>

                </div>

                <!-- ПРОДАВАЧ -->
                <div class="p-6 md:p-7">

                    <div class="border-t border-gray-200 pt-6">

                        <h2 class="text-xl md:text-2xl font-bold text-slate-900 mb-6">
                            Връзки с продавача
                        </h2>

                        <!-- ПРОФИЛ -->
                        <div class="flex items-center gap-4 mb-7">

                            <div class="w-16 h-16 shrink-0 bg-orange-100 rounded-full flex items-center justify-center text-orange-600 text-2xl font-bold">
                                И
                            </div>

                            <div>
                                <h3 class="text-2xl font-bold text-slate-900">
                                    Ивайло
                                </h3>

                                <p class="text-gray-500">
                                    Частен продавач
                                </p>
                            </div>

                        </div>

                        <!-- КОНТАКТИ -->
                        <div class="flex flex-col gap-5">

                            <div class="flex items-center gap-4 border-b border-gray-100 pb-4">

                                <div class="w-11 h-11 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-xl">
                                    📞
                                </div>

                                <div>
                                    <p class="text-sm text-gray-500">
                                        Телефон
                                    </p>

                                    <p class="font-semibold text-slate-900">
                                        Не е посочен
                                    </p>
                                </div>

                            </div>

                            <div class="flex items-center gap-4 border-b border-gray-100 pb-4">

                                <div class="w-11 h-11 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-xl">
                                    ✉️
                                </div>

                                <div>
                                    <p class="text-sm text-gray-500">
                                        Имейл
                                    </p>

                                    <p class="font-semibold text-slate-900">
                                        Не е посочен
                                    </p>
                                </div>

                            </div>

                            <div class="flex items-center gap-4">

                                <div class="w-11 h-11 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-xl">
                                    📅
                                </div>

                                <div>
                                    <p class="text-sm text-gray-500">
                                        Публикувана
                                    </p>

                                    <p class="font-semibold text-slate-900">
                                        18.11.2026 г.
                                    </p>
                                </div>

                            </div>

                        </div>

                    </div>

                </div>

            </div>

        </div>

    </div>

    <!-- ОПИСАНИЕ -->
    <section class="bg-white border border-gray-100 rounded-3xl shadow-xl p-6 md:p-9 mb-6">

        <div class="flex items-center gap-4 mb-6">

            <div class="w-12 h-12 shrink-0 bg-orange-50 rounded-xl flex items-center justify-center">

                <svg
                    class="w-7 h-7 text-orange-600"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                >
                    <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" />
                    <path d="M14 2v6h6" />
                    <path d="M8 13h8" />
                    <path d="M8 17h8" />
                </svg>

            </div>

            <h2 class="text-2xl md:text-3xl font-bold text-slate-900">
                Описание
            </h2>

        </div>

        <div class="border-l-4 border-orange-500 pl-5">

            <p class="text-lg md:text-xl text-slate-700 leading-relaxed">
                Продава се Range Rover Velar 2019 г. – стилен и луксозен SUV,
                съчетаващ комфорт, мощност и модерен дизайн.
                Автомобилът е с 2.0 дизелов двигател, 240 к.с.,
                автоматична скоростна кутия и задвижване 4x4.
                Пробег: 85 000 км. Отличен избор както за градско
                шофиране, така и за дълги пътувания.
            </p>

        </div>

    </section>

    <!-- ОФИЦИАЛЕН САЙТ -->
    <a
        href="https://www.landrover.bg/range-rover/overview"
        target="_blank"
        rel="noopener noreferrer"
        class="group flex items-center justify-between gap-4 bg-white hover:bg-orange-50 border border-orange-100 rounded-2xl shadow-md hover:shadow-lg px-6 py-5 transition-all mb-10"
    >

        <div class="flex items-center gap-4">

            <div class="w-12 h-12 shrink-0 bg-orange-100 rounded-xl flex items-center justify-center text-orange-600 text-2xl">
                ↗
            </div>

            <span class="font-bold text-orange-600 text-lg md:text-xl">
                Официален сайт на производителя
            </span>

        </div>

        <span class="text-orange-600 text-2xl group-hover:translate-x-1 transition-transform">
            →
        </span>

    </a>

</div>
