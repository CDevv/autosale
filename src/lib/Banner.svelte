<script lang="ts">
    import heroImage from "./assets/hero-banner-ready.png";
</script>

<div
    class="relative w-full overflow-hidden rounded-2xl shadow-xl mb-6 bg-black"
>
    <!-- Широката снимка с Peugeot и Ford -->
    <img src={heroImage} alt="Peugeot и Ford" class="block w-full h-auto" />

    <!-- Текст и бутон -->
    <div
        class="absolute inset-0 z-10 flex flex-col justify-center items-start px-5 md:px-10 lg:px-14"
    >
        <h1
            class="text-xl sm:text-3xl md:text-4xl lg:text-5xl font-bold text-white leading-tight mb-2 lg:mb-4"
        >
            Добре дошли в
            <span class="block text-orange-500"> autosale.bg </span>
        </h1>

        <p
            class="text-xs sm:text-sm md:text-base lg:text-xl text-white max-w-md mb-2 lg:mb-5"
        >
            Открийте богат избор от автомобили от частни продавачи и дилъри в
            цяла България.
        </p>

        <a
            href="/offers"
            class="inline-flex items-center gap-2 bg-orange-600 hover:bg-orange-500 text-white text-xs sm:text-sm lg:text-lg font-bold px-4 lg:px-7 py-2 lg:py-3 rounded-xl transition-colors"
        >
            Разгледай обяви
            <span>→</span>
        </a>
    </div>
</div>
