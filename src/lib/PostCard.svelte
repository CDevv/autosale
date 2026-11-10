<script lang="ts">
    import moment from "moment";

    const postDate = moment().locale("bg").startOf("day").fromNow();
</script>

<a class="card hover:underline" href="/post">
    <h3 class="text-2xl">Публикация</h3>
    <p>Автор: Ивайло</p>
    <p>{postDate}</p>
    <div class="text-2xl flex flex-row gap-2">
        <div>
            <span class="icon-[iconoven--heart]"></span> 2
        </div>
        <div>
            <span class="icon-[iconoven--comment]"></span> 1
        </div>
    </div>
</a>
