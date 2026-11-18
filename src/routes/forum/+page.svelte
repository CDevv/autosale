
<script lang="ts">
    import PostCard from "#lib/PostCard.svelte";

    let search = $state("");
    let appliedSearch = $state("");

    let showPost = $derived(
        appliedSearch.trim() === "" ||
        "публикация ивайло".includes(
            appliedSearch.trim().toLocaleLowerCase("bg-BG")
        )
    );
</script>

<div class="max-w-[1450px] mx-auto px-4 md:px-6 py-6">

    <!-- ГОЛЯМ БАНЕР -->
    <section class="relative overflow-hidden rounded-3xl bg-slate-950 shadow-2xl mb-6 min-h-[270px]">

        <!-- Красив тъмен фон -->
        <div class="absolute inset-0 bg-gradient-to-br from-[#090e1d] via-[#161b2b] to-[#3b170d]"></div>

        <!-- Оранжеви светлинни ефекти -->
        <div class="absolute -right-24 -top-40 w-[500px] h-[500px] bg-orange-600/25 blur-3xl rounded-full"></div>
        <div class="absolute right-32 -bottom-48 w-[450px] h-[350px] bg-orange-500/20 blur-3xl rounded-full"></div>

        <!-- Декоративни кръгове -->
        <div class="absolute -right-28 -top-40 w-[580px] h-[580px] border border-orange-500/20 rounded-full"></div>
        <div class="absolute -right-10 -top-16 w-[400px] h-[400px] border border-orange-500/20 rounded-full"></div>

        <!-- Голям декоративен символ -->
        <svg
            class="absolute right-12 top-10 w-48 h-48 md:w-64 md:h-64 text-orange-500/15"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1"
            stroke-linecap="round"
            stroke-linejoin="round"
        >
            <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z" />
        </svg>

        <!-- Оранжева линия -->
        <div class="absolute top-0 left-0 w-2 h-full bg-gradient-to-b from-orange-400 to-orange-600"></div>

        <!-- Съдържание -->
        <div class="relative z-10 px-8 md:px-14 py-12 md:py-14">

            <div class="flex items-center gap-4 mb-5">

                <div class="w-14 h-14 flex items-center justify-center bg-orange-500/15 rounded-2xl border border-orange-500/20">

                    <svg
                        class="w-8 h-8 text-orange-500"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z" />
                    </svg>

                </div>

                <h1 class="text-4xl md:text-6xl font-black text-white">
                    Форуми<span class="text-orange-500"></span>
                </h1>

            </div>

            <p class="text-lg md:text-xl text-gray-300 max-w-2xl leading-relaxed">
                Обсъждайте автомобили, задавайте въпроси
                и споделяйте своя опит с общността на autosale.bg
            </p>

        </div>
    </section>

    <!-- ПРАВИЛА НА ФОРУМА -->
    <section class="bg-white rounded-3xl shadow-xl border border-gray-100 p-6 md:p-9 mb-6">

        <div class="flex items-start gap-5">

            <!-- Икона -->
            <div class="hidden sm:flex shrink-0 w-16 h-16 bg-orange-50 rounded-2xl items-center justify-center">

                <svg
                    class="w-9 h-9 text-orange-600"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                >
                    <circle cx="12" cy="12" r="10" />
                    <path d="M12 16v-4" />
                    <path d="M12 8h.01" />
                </svg>

            </div>

            <div class="flex-1">

                <h2 class="text-2xl md:text-3xl font-bold text-slate-900 mb-2">
                    Добре дошли във форума на autosale.bg!
                </h2>

                <p class="text-gray-500 text-base md:text-lg mb-6">
                    Молим Ви да спазвате някои основни правила:
                </p>

                <!-- Правила -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">

                    <div class="flex items-center gap-3 bg-gray-50 rounded-xl p-4">
                        <span class="w-8 h-8 shrink-0 rounded-full bg-orange-500 text-white flex items-center justify-center font-bold">
                            ✓
                        </span>
                        <span class="text-gray-800 font-medium">
                            Спазвайте добрия тон
                        </span>
                    </div>

                    <div class="flex items-center gap-3 bg-gray-50 rounded-xl p-4">
                        <span class="w-8 h-8 shrink-0 rounded-full bg-orange-500 text-white flex items-center justify-center font-bold">
                            ✓
                        </span>
                        <span class="text-gray-800 font-medium">
                            Не се толерира омраза към други лица
                        </span>
                    </div>

                    <div class="flex items-center gap-3 bg-gray-50 rounded-xl p-4 md:col-span-2">
                        <span class="w-8 h-8 shrink-0 rounded-full bg-orange-500 text-white flex items-center justify-center font-bold">
                            ✓
                        </span>
                        <span class="text-gray-800 font-medium">
                            Не качвайте съдържание, което не е свързано с темата на сайта
                        </span>
                    </div>

                </div>

            </div>

        </div>
    </section>

    <!-- ТЪРСАЧКА -->
    <section class="bg-white rounded-3xl shadow-xl border border-gray-100 p-4 md:p-6 mb-9">

        <form
            class="flex flex-col md:flex-row gap-4"
            onsubmit={(event) => {
                event.preventDefault();
                appliedSearch = search;
            }}
        >

            <div class="relative flex-1">

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
                    placeholder="Търсене във форума..."
                    aria-label="Търсене във форума"
                    class="w-full h-14 bg-gray-50 border-2 border-gray-200 focus:border-orange-500 focus:outline-none rounded-2xl pl-14 pr-5 text-lg text-gray-900"
                />

            </div>

            <button
                type="submit"
                class="h-14 md:min-w-48 bg-gradient-to-r from-orange-600 to-orange-500 hover:from-orange-500 hover:to-orange-400 text-white text-lg font-bold rounded-2xl shadow-md cursor-pointer transition-colors"
            >
                Търсене →
            </button>

        </form>

    </section>

    <!-- ПУБЛИКАЦИИ -->
    <section class="mb-12">

        <div class="flex items-center justify-between gap-4 mb-5">

            <h2 class="flex items-center gap-4 text-2xl md:text-3xl font-bold text-slate-900">
                <span class="w-1.5 h-9 rounded-full bg-orange-600"></span>
                Публикации
            </h2>

        </div>

        {#if showPost}
            <div class="bg-white rounded-3xl shadow-lg hover:shadow-xl border border-gray-100 transition-shadow overflow-hidden">

                <div class="h-1 bg-gradient-to-r from-orange-600 via-orange-400 to-transparent"></div>

                <div class="flex items-start gap-5 p-5 md:p-7">

                    <!-- Икона на публикация -->
                    <div class="hidden sm:flex w-16 h-16 shrink-0 bg-orange-50 rounded-2xl items-center justify-center">

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
                            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" />
                            <path d="M14 2v6h6" />
                            <path d="M8 13h8" />
                            <path d="M8 17h8" />
                        </svg>

                    </div>

                    <!-- Оригиналният компонент -->
                    <div class="flex-1 min-w-0 [&_.card]:border-0 [&_.card]:p-0 [&_.card]:bg-transparent [&_a]:hover:text-orange-600">
                        <PostCard />
                    </div>

                </div>

            </div>
        {:else}
            <div class="bg-white rounded-3xl shadow-lg p-10 text-center">
                <h3 class="text-xl font-bold text-slate-900">
                    Няма намерени публикации
                </h3>
                <p class="text-gray-500 mt-2">
                    Опитайте с друго заглавие или автор.
                </p>
            </div>
        {/if}

    </section>

</div>
