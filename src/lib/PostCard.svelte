<script lang="ts">
    import moment from "moment";

    const postDate = moment().locale("bg").startOf("day").fromNow();
</script>

<a class="card hover:underline" href="/post">
    <h3 class="text-3xl">Публикация</h3>
    <p class="text-2xl">Автор: Ивайло</p>
    <p class="text-2xl">{postDate}</p>
    <div class="text-2xl flex flex-row gap-2">
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
                <path
                    d="M21 11.5a8.5 8.5 0 0 1-8.5 8.5 8.5 8.5 0 0 1-4-.9L3 21l1.9-5.5a8.5 8.5 0 1 1 16.1-4Z"
                />
            </svg>

            <span>1 коментар</span>
        </div>

        <!-- Харесвания -->
        <div
            class="flex items-center gap-2 bg-orange-50 text-orange-600 rounded-xl px-4 py-2"
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
                <path
                    d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8L12 21l8.8-8.6a5.5 5.5 0 0 0 0-7.8Z"
                />
            </svg>

            <span class="font-bold">2</span>
        </div>
    </div>
</a>
