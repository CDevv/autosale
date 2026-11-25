<svelte:head>
    <title>Autosale.bg - Контакти</title>
</svelte:head>

<section
    class="bg-white rounded-3xl shadow-2xl border border-gray-100 overflow-hidden"
>
    <div class="grid grid-cols-1 lg:grid-cols-2">
        <!-- ЛЯВА ЧАСТ -->
        <div
            class="bg-slate-50 p-8 md:p-10 border-b lg:border-b-0 lg:border-r border-gray-200"
        >
            <h2 class="text-3xl md:text-4xl font-bold text-slate-900 mt-3 mb-5">
                Как можем да помогнем?
            </h2>

            <p class="text-gray-500 text-lg leading-relaxed mb-8 max-w-md">
                Свържи се с нас относно автомобилните обяви, използването на
                платформата или предложения за подобрения.
            </p>

            <div class="space-y-4">
                <div
                    class="flex items-start gap-4 bg-white rounded-2xl border border-gray-100 shadow-sm p-5"
                >
                    <div
                        class="w-12 h-12 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-orange-600 text-2xl"
                    >
                        ✉
                    </div>

                    <div>
                        <h3 class="text-xl font-bold text-slate-900 mb-1">
                            Въпроси
                        </h3>

                        <p class="text-gray-500">
                            Попитай ни за платформата и нейните възможности.
                        </p>
                    </div>
                </div>

                <div
                    class="flex items-start gap-4 bg-white rounded-2xl border border-gray-100 shadow-sm p-5"
                >
                    <div
                        class="w-12 h-12 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-orange-600 text-2xl"
                    >
                        💡
                    </div>

                    <div>
                        <h3 class="text-xl font-bold text-slate-900 mb-1">
                            Предложения
                        </h3>

                        <p class="text-gray-500">
                            Сподели идея за подобряване на autosale.bg.
                        </p>
                    </div>
                </div>

                <div
                    class="flex items-start gap-4 bg-white rounded-2xl border border-gray-100 shadow-sm p-5"
                >
                    <div
                        class="w-12 h-12 shrink-0 rounded-xl bg-orange-50 flex items-center justify-center text-orange-600 text-2xl"
                    >
                        ?
                    </div>

                    <div>
                        <h3 class="text-xl font-bold text-slate-900 mb-1">
                            Съдействие
                        </h3>

                        <p class="text-gray-500">
                            Опиши проблема, за който имаш нужда от помощ.
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- ДЯСНА ЧАСТ -->
        <div class="p-8 md:p-10">
            <div class="flex items-center gap-4 mb-8">
                <div
                    class="w-14 h-14 rounded-2xl bg-orange-500 text-white flex items-center justify-center text-2xl shadow-lg shadow-orange-500/20"
                >
                    💬
                </div>

                <div>
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">
                        Изпрати ни съобщение
                    </h2>

                    <p class="text-gray-500 mt-1">
                        Попълни формата за контакт.
                    </p>
                </div>
            </div>

            <form class="flex flex-col gap-5">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
                    <div class="flex flex-col gap-2">
                        <label for="name" class="font-semibold text-slate-900">
                            Име <span class="text-orange-600">*</span>
                        </label>

                        <input
                            id="name"
                            name="name"
                            type="text"
                            required
                            placeholder="Вашето име"
                            class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-4 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                        />
                    </div>

                    <div class="flex flex-col gap-2">
                        <label for="email" class="font-semibold text-slate-900">
                            Имейл <span class="text-orange-600">*</span>
                        </label>

                        <input
                            id="email"
                            name="email"
                            type="email"
                            required
                            placeholder="Вашият имейл"
                            class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-4 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                        />
                    </div>
                </div>

                <div class="flex flex-col gap-2">
                    <label for="title" class="font-semibold text-slate-900">
                        Тема <span class="text-orange-600">*</span>
                    </label>

                    <input
                        id="title"
                        name="title"
                        type="text"
                        required
                        placeholder="Тема на съобщението"
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-4 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors"
                    />
                </div>

                <div class="flex flex-col gap-2">
                    <label for="content" class="font-semibold text-slate-900">
                        Съобщение <span class="text-orange-600">*</span>
                    </label>

                    <textarea
                        id="content"
                        name="content"
                        rows="7"
                        required
                        placeholder="Напишете вашето съобщение тук..."
                        class="w-full rounded-xl border-2 border-gray-200 bg-gray-50 px-4 py-3.5 text-slate-900 outline-none focus:border-orange-500 focus:bg-white transition-colors resize-none"
                    ></textarea>
                </div>

                <button
                    type="submit"
                    class="w-full rounded-2xl bg-orange-500 hover:bg-orange-600 text-white text-xl font-bold py-4 transition-colors shadow-lg shadow-orange-500/20"
                >
                    Изпрати съобщение
                </button>
            </form>
        </div>
    </div>
</section>
