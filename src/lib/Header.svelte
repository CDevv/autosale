<header
    class="fixed top-0 w-full bg-gradient-to-r from-orange-700 via-orange-500 to-orange-600 shadow-md z-10"
>
    <div
        class="max-w-[1450px] mx-auto h-16 flex items-center justify-between gap-4 px-4 md:px-6"
    >
        <!-- Лого -->
        <a
            href="/"
            class="shrink-0 bg-white text-gray-900 text-xl font-bold px-3 py-2 rounded-xl shadow-sm"
        >
            <span class="text-orange-600">auto</span>sale.bg
        </a>

        <!-- Меню -->
        <nav class="hidden lg:flex items-center gap-8 grow ml-1">
            <a
                href="/"
                class="text-white text-xl font-semibold hover:text-orange-100 transition-colors"
            >
                Начало
            </a>

            <a
                href="/dealers"
                class="text-white text-xl font-semibold hover:text-orange-100 transition-colors"
            >
                Дилъри
            </a>

            <a
                href="/offers"
                class="text-white text-xl font-semibold hover:text-orange-100 transition-colors"
            >
                Обяви
            </a>

            <a
                href="/forum"
                class="text-white text-xl font-semibold hover:text-orange-100 transition-colors"
            >
                Форум
            </a>

            <a
                href="/contact"
                class="text-white text-xl font-semibold hover:text-orange-100 transition-colors"
            >
                Контакти
            </a>
        </nav>

        <!-- Регистрация -->
        <a
            href="/register"
            class="shrink-0 flex items-center justify-center gap-2 border-2 border-white text-white text-base md:text-lg font-semibold px-4 md:px-6 py-2 rounded-2xl hover:bg-white hover:text-orange-600 transition-colors"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                width="22"
                height="22"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
            >
                <path d="M20 21a8 8 0 0 0-16 0" />
                <circle cx="12" cy="7" r="4" />
            </svg>

            <span>Регистрация</span>
        </a>
    </div>

    <!-- Навигация за малки екрани -->
    <nav
        class="lg:hidden flex items-center gap-6 overflow-x-auto px-4 pb-3 text-white font-semibold whitespace-nowrap"
    >
        <a href="/">Начало</a>
        <a href="/dealers">Дилъри</a>
        <a href="/offers">Обяви</a>
        <a href="/forum">Форум</a>
        <a href="/contact">Контакти</a>
    </nav>
</header>
