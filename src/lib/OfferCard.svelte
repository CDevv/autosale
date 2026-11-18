
<script lang="ts">
    import image from "#lib/assets/21764003891272177_bw.webp";
</script>

<div class="bg-white rounded-2xl shadow-lg border border-gray-100 p-4 w-full">

    <div class="flex flex-col sm:flex-row gap-5">

        <div class="w-full sm:w-64 h-44 shrink-0">
            <img
                src={image}
                alt="Колата на Ивайло"
                class="w-full h-full object-cover rounded-xl"
            />
        </div>

        <div class="flex flex-col justify-center items-start gap-4">

            <h2 class="text-2xl font-bold text-gray-900">
                Колата на Ивайло
            </h2>

            <p class="text-3xl font-bold text-orange-600">
                €50
            </p>

            <a
                href="/offer"
                class="bg-orange-600 hover:bg-orange-500 text-white text-lg font-bold px-8 py-3 rounded-xl transition-colors"
            >
                Разгледай →
            </a>

        </div>
    </div>
</div>
