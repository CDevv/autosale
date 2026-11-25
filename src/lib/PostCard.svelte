<script lang="ts">
    import moment from "moment";
    import CommentsTag from "./CommentsTag.svelte";
    import LikesTag from "./LikesTag.svelte";

    const postDate = moment().locale("bg").startOf("day").fromNow();
</script>

<a class="card hover:underline" href="/post">
    <h3 class="text-3xl">Публикация</h3>
    <p class="text-2xl">Автор: Ивайло</p>
    <p class="text-2xl">{postDate}</p>
    <br />
    <div class="text-2xl flex flex-row gap-2">
        <!-- Харесвания -->
        <LikesTag />

        <!-- Коментари -->
        <CommentsTag />
    </div>
</a>
