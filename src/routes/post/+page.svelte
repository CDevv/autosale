<script lang="ts">
    import moment from "moment";

    const postDate = moment().locale("bg").startOf("day").fromNow();
</script>

<h1 class="text-3xl">Публикация</h1>
<br />
<div class="card p-4">
    <p class="text-2xl">Автор: Ивайло</p>
    <p class="text-2xl">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque quidem
        facilis voluptate ipsum officiis asperiores aliquid unde! Voluptatem,
        nostrum! Tempore quisquam voluptatum dicta officia pariatur minus
        aliquam atque sunt eum.
    </p>
    <br />
    <div class="text-2xl flex flex-row gap-2">
        <div>
            <span class="icon-[iconoven--heart]"></span> 2
        </div>
        <div>
            <span class="icon-[iconoven--comment]"></span> 1
        </div>
    </div>
    <p class="text-2xl">
        {postDate}
    </p>
</div>
<br />
<h2 class="text-3xl">Коментари</h2>
<br />
<div>
    <div class="card">
        <h3 class="text-3xl">Автор: Гошо</h3>
        <p class="text-2xl">Не вярвайте на този продавач!</p>
        <br />
        <div class="text-2xl flex flex-row gap-2">
            <div>
                <span class="icon-[iconoven--heart]"></span> 2
            </div>
            <div>
                <span class="icon-[iconoven--comment]"></span> 1
            </div>
        </div>
        <p class="text-2xl">{postDate}</p>
    </div>
</div>
