
<script lang="ts">


    let message = $state("");

    function handleLogin(event: SubmitEvent) {
        event.preventDefault();

        message = "За реално влизане е необходимо да свържеш формата със система за удостоверяване.";
    }
</script>

<div class="max-w-[1400px] mx-auto px-4 md:px-6 py-8 md:py-12">

    <div class="grid grid-cols-1 lg:grid-cols-5 gap-6 items-stretch">

        <!-- ЛЯВА ЧАСТ - ВЛИЗАНЕ -->
        <section class="lg:col-span-3 bg-white rounded-3xl shadow-2xl border border-gray-100 p-6 sm:p-8 md:p-10">

            <!-- ЗАГЛАВИЕ -->
            <div class="flex items-center gap-4 mb-9">

                <div class="w-16 h-16 shrink-0 bg-gradient-to-br from-orange-500 to-orange-600 rounded-2xl flex items-center justify-center shadow-lg shadow-orange-500/20">

                    <svg
                        class="w-9 h-9 text-white"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M10 17l5-5-5-5" />
                        <path d="M15 12H3" />
                        <path d="M12 3h6a3 3 0 0 1 3 3v12a3 3 0 0 1-3 3h-6" />
                    </svg>

                </div>

                <div>
                    <h1 class="text-3xl md:text-4xl font-black text-slate-900">
                        Влизане
                    </h1>

                    <p class="text-gray-500 mt-2">
                        Добре дошъл отново в autosale.bg
                    </p>
                </div>

            </div>

            <!-- ФОРМА -->
            <form onsubmit={handleLogin} class="flex flex-col gap-6">

                <!-- ИМЕ -->
                <div>
                    <label for="login-name" class="block font-bold text-slate-900 mb-2">
                        Име
                    </label>

                    <input
                        id="login-name"
                        name="name"
                        type="text"
                        autocomplete="username"
                        required
                        placeholder="Въведи своето име"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ИМЕЙЛ -->
                <div>
                    <label for="login-email" class="block font-bold text-slate-900 mb-2">
                        Имейл
                    </label>

                    <input
                        id="login-email"
                        name="email"
                        type="email"
                        autocomplete="email"
                        required
                        placeholder="Въведи своя имейл"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ПАРОЛА -->
                <div>
                    <label for="login-pass" class="block font-bold text-slate-900 mb-2">
                        Парола
                    </label>

                    <input
                        id="login-pass"
                        name="pass"
                        type="password"
                        autocomplete="current-password"
                        required
                        placeholder="Въведи своята парола"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                {#if message}
                    <p class="text-sm text-orange-700 bg-orange-50 border border-orange-200 rounded-xl p-3" role="status">
                        {message}
                    </p>
                {/if}

                <!-- БУТОН -->
                <button
                    type="submit"
                    class="w-full mt-2 rounded-2xl bg-gradient-to-r from-orange-600 to-orange-500 hover:from-orange-500 hover:to-orange-400 py-4 text-white text-lg font-bold shadow-lg shadow-orange-500/20 cursor-pointer transition-colors"
                >
                    Влез в профила →
                </button>

            </form>

            <!-- РЕГИСТРАЦИЯ -->
            <div class="mt-8 rounded-2xl bg-orange-50 border border-orange-100 px-5 py-5 text-center">

                <p class="text-slate-700">
                    Нямате профил?

                    <a
                        href="/register"
                        class="font-bold text-orange-600 hover:text-orange-700"
                    >
                        Регистрирайте се
                    </a>
                </p>

            </div>

        </section>

        <!-- ДЯСНА ЧАСТ -->
        <aside class="lg:col-span-2 relative min-h-[450px] lg:min-h-full overflow-hidden rounded-3xl bg-slate-950 shadow-2xl">


            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-950/80 to-slate-900/20"></div>

            <div class="relative z-10 h-full min-h-[450px] flex flex-col justify-between p-8 md:p-10">

                <!-- ЗАГЛАВИЕ -->
                <div>

                    <div class="w-14 h-1 bg-orange-500 rounded-full mb-6"></div>

                    <h2 class="text-3xl md:text-4xl font-black text-white leading-tight">
                        Добре дошъл в
                        <span class="text-orange-500">
                            autosale.bg
                        </span>
                    </h2>

                    <p class="text-lg text-gray-200 leading-relaxed mt-5">
                        Влез в своя профил и продължи да разглеждаш
                        автомобилите и обявите.
                    </p>

                </div>

                <!-- ПРЕДИМСТВА -->
                <div class="space-y-6 mt-12">

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 bg-orange-600 rounded-2xl flex items-center justify-center text-2xl">
                            🚗
                        </div>

                        <div>
                            <h3 class="text-white font-bold text-lg">
                                Автомобилни обяви
                            </h3>

                            <p class="text-sm text-gray-300">
                                Разглеждай предложенията
                            </p>
                        </div>

                    </div>

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 bg-orange-600 rounded-2xl flex items-center justify-center text-2xl">
                            📝
                        </div>

                        <div>
                            <h3 class="text-white font-bold text-lg">
                                Публикуване на обяви
                            </h3>

                            <p class="text-sm text-gray-300">
                                Добави своя автомобил
                            </p>
                        </div>

                    </div>

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 bg-orange-600 rounded-2xl flex items-center justify-center text-2xl">
                            💬
                        </div>

                        <div>
                            <h3 class="text-white font-bold text-lg">
                                Автомобилен форум
                            </h3>

                            <p class="text-sm text-gray-300">
                                Участвай в дискусии
                            </p>
                        </div>

                    </div>

                </div>

            </div>

        </aside>

    </div>

</div>
