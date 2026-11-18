
<script lang="ts">
   

    let password = $state("");
    let passwordRepeat = $state("");
    let message = $state("");

    function handleRegister(event: SubmitEvent) {
        event.preventDefault();

        if (password !== passwordRepeat) {
            message = "Паролите не съвпадат.";
            return;
        }

        message = "Формата е попълнена. За реална регистрация е необходима връзка със сървър.";
    }
</script>

<div class="max-w-[1400px] mx-auto px-4 md:px-6 py-8 md:py-12">

    <div class="grid grid-cols-1 lg:grid-cols-5 gap-6 items-stretch">

        <!-- ЛЯВА ЧАСТ - РЕГИСТРАЦИЯ -->
        <section class="lg:col-span-3 bg-white rounded-3xl shadow-2xl border border-gray-100 p-6 sm:p-8 md:p-10">

            <!-- ЗАГЛАВИЕ -->
            <div class="flex items-center gap-4 mb-9">

                <div class="w-16 h-16 shrink-0 bg-gradient-to-br from-orange-500 to-orange-600 rounded-2xl flex items-center justify-center shadow-lg shadow-orange-500/20">

                    <svg
                        class="w-9 h-9 text-white"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        stroke-width="2"
                    >
                        <circle cx="10" cy="7" r="4" />
                        <path d="M3 21v-2a7 7 0 0 1 14 0v2" />
                        <path d="M19 6v6M16 9h6" />
                    </svg>

                </div>

                <div>
                    <h1 class="text-3xl md:text-4xl font-black text-slate-900">
                        Регистрация
                    </h1>

                    <p class="text-gray-500 mt-2">
                        Създай своя акаунт в autosale.bg
                    </p>
                </div>

            </div>

            <!-- ФОРМА -->
            <form onsubmit={handleRegister} class="flex flex-col gap-5">

                <!-- ИМЕ -->
                <div>
                    <label for="register-name" class="block font-bold text-slate-900 mb-2">
                        Име
                    </label>

                    <input
                        id="register-name"
                        name="name"
                        type="text"
                        autocomplete="name"
                        required
                        placeholder="Въведи своето име"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ИМЕЙЛ -->
                <div>
                    <label for="register-email" class="block font-bold text-slate-900 mb-2">
                        Имейл
                    </label>

                    <input
                        id="register-email"
                        name="email"
                        type="email"
                        autocomplete="email"
                        required
                        placeholder="Въведи своя имейл"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ТЕЛЕФОН -->
                <div>
                    <label for="register-phone" class="block font-bold text-slate-900 mb-2">
                        Телефон
                    </label>

                    <input
                        id="register-phone"
                        name="phone"
                        type="tel"
                        autocomplete="tel"
                        required
                        placeholder="Въведи телефонен номер"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ПАРОЛА -->
                <div>
                    <label for="register-pass" class="block font-bold text-slate-900 mb-2">
                        Парола
                    </label>

                    <input
                        id="register-pass"
                        name="pass"
                        type="password"
                        autocomplete="new-password"
                        required
                        minlength="8"
                        bind:value={password}
                        placeholder="Въведи парола"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-5 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <!-- ПОВТОРИ ПАРОЛА -->
                <div>
                    <label for="register-passrepeat" class="block font-bold text-slate-900 mb-2">
                        Повтори парола
                    </label>

                    <input
                        id="register-passrepeat"
                        name="passrepeat"
                        type="password"
                        autocomplete="new-password"
                        required
                        minlength="8"
                        bind:value={passwordRepeat}
                        placeholder="Повтори паролата"
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
                    class="w-full mt-3 rounded-2xl bg-gradient-to-r from-orange-600 to-orange-500 hover:from-orange-500 hover:to-orange-400 py-4 text-white text-lg font-bold shadow-lg shadow-orange-500/20 cursor-pointer transition-colors"
                >
                    Регистрирай се →
                </button>

            </form>

            <!-- ВЛИЗАНЕ -->
            <div class="mt-6 rounded-2xl bg-orange-50 border border-orange-100 px-5 py-5 text-center">

                <p class="text-slate-700">
                    Вече имате профил?

                    <a
                        href="/login"
                        class="font-bold text-orange-600 hover:text-orange-700"
                    >
                        Влезте
                    </a>
                </p>

            </div>

        </section>

        <!-- ДЯСНА ЧАСТ - АВТОМОБИЛ -->
        <aside class="lg:col-span-2 relative min-h-[460px] lg:min-h-full overflow-hidden rounded-3xl bg-slate-950 shadow-2xl">

           

            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-950/80 to-slate-900/20"></div>

            <div class="relative z-10 h-full min-h-[460px] flex flex-col justify-between p-8 md:p-10">

                <!-- ГОРЕН ТЕКСТ -->
                <div>

                    <div class="w-14 h-1 bg-orange-500 rounded-full mb-6"></div>

                    <h2 class="text-3xl md:text-4xl font-black text-white leading-tight">
                        Присъедини се към
                        <span class="text-orange-500">autosale.bg</span>
                    </h2>

                    <p class="text-gray-200 mt-5 text-lg leading-relaxed">
                        Създай профил и откривай автомобили,
                        публикувай обяви и разглеждай предложения.
                    </p>

                </div>

                <!-- ПРЕДИМСТВА -->
                <div class="space-y-6 mt-12">

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 rounded-2xl bg-orange-600 flex items-center justify-center text-2xl">
                            🚗
                        </div>

                        <div>
                            <h3 class="font-bold text-white text-lg">
                                Публикувай обяви
                            </h3>

                            <p class="text-sm text-gray-300">
                                Представи своя автомобил
                            </p>
                        </div>

                    </div>

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 rounded-2xl bg-orange-600 flex items-center justify-center text-2xl">
                            🔎
                        </div>

                        <div>
                            <h3 class="font-bold text-white text-lg">
                                Разглеждай автомобили
                            </h3>

                            <p class="text-sm text-gray-300">
                                Намери подходяща обява
                            </p>
                        </div>

                    </div>

                    <div class="flex items-center gap-4">

                        <div class="w-12 h-12 shrink-0 rounded-2xl bg-orange-600 flex items-center justify-center text-2xl">
                            💬
                        </div>

                        <div>
                            <h3 class="font-bold text-white text-lg">
                                Свързвай се с продавачи
                            </h3>

                            <p class="text-sm text-gray-300">
                                Разглеждай информацията за контакт
                            </p>
                        </div>

                    </div>

                </div>

            </div>

        </aside>

    </div>

</div>
