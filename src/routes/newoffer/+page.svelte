<script lang="ts">
    import ImageListInput from "#lib/ImageListInput.svelte";

    let input: HTMLInputElement | undefined = $state();
</script>

<svelte:head>
    <title>Autosale.bg - Нова обява</title>
</svelte:head>

<!-- ОСНОВНА СЕКЦИЯ -->
<section
    class="bg-white rounded-3xl shadow-2xl border border-gray-100 overflow-hidden mb-12"
>
    <div class="grid grid-cols-1 lg:grid-cols-5">
        <!-- ЛЯВА ЧАСТ -->
        <div
            class="lg:col-span-2 bg-gradient-to-b from-orange-50/70 to-slate-50 p-7 md:p-10 border-b lg:border-b-0 lg:border-r border-gray-200"
        >
            <!-- Заглавие -->
            <div class="flex items-center gap-3 mb-9">
                <span class="w-1.5 h-9 bg-orange-600 rounded-full"></span>

                <h2 class="text-2xl md:text-3xl font-bold text-slate-900">
                    Стъпки за публикуване
                </h2>
            </div>

            <!-- СТЪПКА 1 -->
            <div class="flex items-start gap-4 mb-9">
                <div
                    class="w-14 h-14 shrink-0 rounded-2xl bg-orange-100 flex items-center justify-center"
                >
                    <svg
                        class="w-8 h-8 text-orange-600"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M5 17h14l1-5-2-5H6l-2 5 1 5Z" />
                        <path d="M5 17v2M19 17v2" />
                        <path d="M4 12h16" />
                        <circle cx="7" cy="15" r="1" />
                        <circle cx="17" cy="15" r="1" />
                    </svg>
                </div>

                <div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">
                        1. Попълни данните
                    </h3>

                    <p class="text-gray-500 leading-relaxed">
                        Въведи модела и описание на автомобила.
                    </p>
                </div>
            </div>

            <!-- СТЪПКА 2 -->
            <div class="flex items-start gap-4 mb-9">
                <div
                    class="w-14 h-14 shrink-0 rounded-2xl bg-orange-100 flex items-center justify-center"
                >
                    <svg
                        class="w-8 h-8 text-orange-600"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <rect x="3" y="3" width="18" height="18" rx="2" />
                        <circle cx="8.5" cy="8.5" r="1.5" />
                        <path d="m21 15-5-5L5 21" />
                    </svg>
                </div>

                <div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">
                        2. Добави снимки
                    </h3>

                    <p class="text-gray-500 leading-relaxed">
                        Избери ясни снимки, които представят автомобила.
                    </p>
                </div>
            </div>

            <!-- СТЪПКА 3 -->
            <div class="flex items-start gap-4">
                <div
                    class="w-14 h-14 shrink-0 rounded-2xl bg-orange-100 flex items-center justify-center"
                >
                    <svg
                        class="w-8 h-8 text-orange-600"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="m5 12 4 4L19 6" />
                    </svg>
                </div>

                <div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2">
                        3. Публикувай
                    </h3>

                    <p class="text-gray-500 leading-relaxed">
                        Прегледай въведената информация и публикувай обявата.
                    </p>
                </div>
            </div>

            <!-- СЪВЕТ -->
            <div class="mt-12 pt-8 border-t border-orange-100">
                <div
                    class="rounded-2xl bg-white border border-orange-100 p-5 shadow-sm"
                >
                    <div class="flex items-center gap-3 mb-2">
                        <span class="text-orange-600 text-2xl">✦</span>

                        <h3 class="font-bold text-slate-900">Съвет</h3>
                    </div>

                    <p class="text-sm text-gray-500 leading-relaxed">
                        Подробното описание и качествените снимки помагат на
                        купувачите да се запознаят с автомобила.
                    </p>
                </div>
            </div>
        </div>

        <!-- ДЯСНА ЧАСТ -->
        <div class="lg:col-span-3 p-7 md:p-10">
            <!-- Заглавие на формата -->
            <div class="flex items-center gap-4 mb-8">
                <div
                    class="w-14 h-14 shrink-0 bg-gradient-to-br from-orange-500 to-orange-600 rounded-2xl flex items-center justify-center shadow-lg shadow-orange-500/20"
                >
                    <svg
                        class="w-8 h-8 text-white"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M5 17h14l1-5-2-5H6l-2 5 1 5Z" />
                        <path d="M5 17v2M19 17v2" />
                        <path d="M4 12h16" />
                        <circle cx="7" cy="15" r="1" />
                        <circle cx="17" cy="15" r="1" />
                    </svg>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-slate-900">
                        Нова обява
                    </h2>

                    <p class="text-gray-500 mt-1">
                        Попълни данните за автомобила.
                    </p>
                </div>
            </div>

            <!-- ФОРМА -->
            <form class="flex flex-col gap-6">
                <!-- МОДЕЛ -->
                <div class="flex flex-col gap-2">
                    <label for="name" class="text-lg font-bold text-slate-900">
                        Модел
                    </label>

                    <div class="relative">
                        <svg
                            class="absolute left-4 top-1/2 -translate-y-1/2 w-6 h-6 text-gray-400 pointer-events-none"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path d="M5 17h14l1-5-2-5H6l-2 5 1 5Z" />
                            <path d="M5 17v2M19 17v2" />
                            <path d="M4 12h16" />
                        </svg>

                        <input
                            id="name"
                            name="name"
                            type="text"
                            class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 py-3.5 pl-14 pr-4 text-lg text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                        />
                    </div>
                </div>

                <!-- ОПИСАНИЕ -->
                <div class="flex flex-col gap-2">
                    <label
                        for="content"
                        class="text-lg font-bold text-slate-900"
                    >
                        Описание
                    </label>

                    <textarea
                        id="content"
                        name="content"
                        rows="5"
                        placeholder="Опиши автомобила – състояние, екстри, километри и друга информация..."
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-4 py-3.5 text-lg text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors resize-y"
                    ></textarea>
                </div>

                <!-- СНИМКИ -->
                <div class="flex flex-col gap-3">
                    <label class="text-lg font-bold text-slate-900">
                        Снимки
                    </label>

                    <div
                        class="rounded-2xl border-2 border-dashed border-gray-300 bg-gray-50 p-5 md:p-7 relative"
                    >
                        <div
                            class="flex flex-col items-center text-center mb-5"
                        >
                            <div
                                class="w-14 h-14 rounded-2xl bg-orange-100 flex items-center justify-center mb-3"
                            >
                                <svg
                                    class="w-8 h-8 text-orange-600"
                                    xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    stroke="currentColor"
                                    stroke-width="2"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                >
                                    <path d="M12 16V4" />
                                    <path d="m7 9 5-5 5 5" />
                                    <path d="M20 16v4H4v-4" />
                                </svg>
                            </div>

                            <h3 class="text-lg font-bold text-slate-900">
                                Добави снимки на автомобила
                            </h3>

                            <p class="text-gray-500 text-sm mt-1">
                                Избери снимки от устройството си.
                            </p>
                        </div>

                        <input
                            bind:this={input}
                            class="card p-0.5 w-full h-36 opacity-0 absolute top-0.5 right-0"
                            type="file"
                            accept=".jpg, .jpeg, .png"
                        />

                        <!-- Твоят компонент за снимките -->
                        <ImageListInput {input} />
                    </div>
                </div>

                <!-- БУТОН ПУБЛИКУВАЙ -->
                <input
                    name="submit"
                    type="submit"
                    value="Публикувай"
                    class="w-full rounded-2xl bg-gradient-to-r from-orange-600 to-orange-500 hover:from-orange-500 hover:to-orange-400 text-white text-xl font-bold py-4 shadow-lg shadow-orange-500/20 transition-colors cursor-pointer"
                />
            </form>
        </div>
    </div>
</section>
