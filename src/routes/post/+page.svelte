
<script lang="ts">
    import moment from "moment";

    const postDate = moment().locale("bg").startOf("day").fromNow();
</script>

<div class="max-w-[1450px] mx-auto px-4 md:px-6 py-8">

    <!-- ВРЪЩАНЕ КЪМ ФОРУМА -->
    <a
        href="/forum"
        class="inline-flex items-center gap-3 bg-white/90 hover:bg-white text-slate-800 font-semibold px-5 py-3 rounded-full shadow-sm border border-gray-100 transition-colors mb-6"
    >
        <svg
            class="w-5 h-5 text-orange-600"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
        >
            <path d="m15 18-6-6 6-6" />
        </svg>

        Обратно към форума
    </a>

    <!-- ЗАГЛАВИЕ -->
    <div class="flex items-center gap-4 mb-7">
        <span class="w-1.5 h-11 rounded-full bg-orange-600"></span>

        <h1 class="text-3xl md:text-5xl font-black text-slate-950">
            Публикация
        </h1>
    </div>

    <!-- ОСНОВНА ПУБЛИКАЦИЯ -->
    <article class="relative bg-white rounded-3xl shadow-xl border border-gray-100 overflow-hidden mb-10">

        <!-- Оранжев акцент -->
        <div class="absolute left-0 top-0 bottom-0 w-1.5 bg-gradient-to-b from-orange-500 to-orange-600"></div>

        <div class="p-6 md:p-10">

            <!-- АВТОР -->
            <div class="flex items-center gap-4 mb-7">

                <!-- Аватар -->
                <div class="w-16 h-16 shrink-0 rounded-full bg-orange-100 flex items-center justify-center">

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
                        <circle cx="12" cy="8" r="4" />
                        <path d="M4 21v-2a8 8 0 0 1 16 0v2" />
                    </svg>

                </div>

                <div class="flex-1">

                    <div class="flex flex-wrap items-center gap-3 mb-1">

                        <h2 class="text-2xl md:text-3xl font-bold text-slate-900">
                            Ивайло
                        </h2>

                        <span class="bg-orange-500 text-white text-xs font-bold px-3 py-1 rounded-full">
                            Автор
                        </span>

                    </div>

                    <p class="text-gray-500">
                        Публикувано {postDate}
                    </p>

                </div>

            </div>

            <!-- ТЕКСТ НА ПУБЛИКАЦИЯТА -->
            <p class="text-lg md:text-xl text-slate-800 leading-relaxed mb-8">
               Продава се Range Rover Velar 2019 г. – стилен и луксозен SUV, съчетаващ комфорт, мощност и модерен дизайн. Автомобилът е с 2.0 дизелов двигател, 240 к.с., автоматична скоростна кутия и задвижване 4x4. Пробег: 85 000 км. Отличен избор както за градско шофиране, така и за дълги пътувания.
            </p>

            <!-- СТАТИСТИКА -->
            <div class="border-t border-gray-200 pt-6 flex flex-wrap items-center gap-4 md:gap-8">

                <!-- Дата -->
                <div class="flex items-center gap-2 text-gray-500">

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
                        <rect x="3" y="5" width="18" height="16" rx="2" />
                        <path d="M16 3v4M8 3v4M3 10h18" />
                    </svg>

                    <span>{postDate}</span>
                </div>

                <!-- Коментари -->
                <div class="flex items-center gap-2 text-gray-500">

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
                        <path d="M21 11.5a8.5 8.5 0 0 1-8.5 8.5 8.5 8.5 0 0 1-4-.9L3 21l1.9-5.5a8.5 8.5 0 1 1 16.1-4Z" />
                    </svg>

                    <span>1 коментар</span>
                </div>

                <!-- Харесвания -->
                <div class="flex items-center gap-2 bg-orange-50 text-orange-600 rounded-xl px-4 py-2">

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
                        <path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8L12 21l8.8-8.6a5.5 5.5 0 0 0 0-7.8Z" />
                    </svg>

                    <span class="font-bold">2</span>
                </div>

            </div>

        </div>
    </article>

    <!-- ЗАГЛАВИЕ КОМЕНТАРИ -->
    <div class="flex items-center gap-4 mb-6">

        <div class="w-11 h-11 rounded-2xl bg-orange-50 flex items-center justify-center">

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
                <path d="M21 11.5a8.5 8.5 0 0 1-8.5 8.5 8.5 8.5 0 0 1-4-.9L3 21l1.9-5.5a8.5 8.5 0 1 1 16.1-4Z" />
            </svg>

        </div>

        <h2 class="text-3xl md:text-4xl font-bold text-slate-900">
            Коментари <span class="text-orange-600">(1)</span>
        </h2>

    </div>

    <!-- КОМЕНТАР -->
    <section class="bg-white rounded-3xl shadow-xl border border-gray-100 overflow-hidden mb-8">

        <div class="p-6 md:p-9">

            <!-- Автор на коментара -->
            <div class="flex items-center gap-4 mb-6">

                <div class="w-14 h-14 shrink-0 rounded-full bg-orange-100 flex items-center justify-center">

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
                        <circle cx="12" cy="8" r="4" />
                        <path d="M4 21v-2a8 8 0 0 1 16 0v2" />
                    </svg>

                </div>

                <div>

                    <h3 class="text-2xl font-bold text-slate-900">
                        Гошо
                    </h3>

                    <p class="text-gray-500">
                        {postDate}
                    </p>

                </div>

            </div>

            <!-- Съдържание -->
            <p class="text-lg md:text-xl text-slate-800 mb-7">
                Не вярвайте на този продавач!
            </p>

            <!-- Статистика -->
            <div class="border-t border-gray-200 pt-5 flex flex-wrap items-center gap-4">

                <div class="flex items-center gap-2 bg-orange-50 text-orange-600 rounded-xl px-4 py-2">

                    <svg
                        class="w-5 h-5"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8L12 21l8.8-8.6a5.5 5.5 0 0 0 0-7.8Z" />
                    </svg>

                    <span class="font-bold">2</span>
                </div>

                <div class="flex items-center gap-2 text-gray-500">

                    <svg
                        class="w-5 h-5"
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M21 11.5a8.5 8.5 0 0 1-8.5 8.5 8.5 8.5 0 0 1-4-.9L3 21l1.9-5.5a8.5 8.5 0 1 1 16.1-4Z" />
                    </svg>

                    <span>1</span>

                </div>

            </div>

        </div>

    </section>

</div>
