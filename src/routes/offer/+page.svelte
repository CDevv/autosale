<script lang="ts">
    import image from "#lib/assets/21764003891272177_bw.webp";
</script>

<div class="flex flex-row gap-2">
    <h1 class="text-3xl mt-0.5 mb-0.5 grow">Име на обява</h1>
    <a href="/" class="button max-w-3xs min-w-2xs text-center"
        >Изпрати запитване</a
    >
</div>
<br />
<div class="flex flex-row gap-2">
    <div class="card min-w-4/6 h-144">
        <div class="h-full max-h-full">
            <img
                class="max-w-full max-h-full object-contain"
                alt="обява"
                src={image}
            />
        </div>
    </div>
    <div class="card flex flex-col gap-2 grow">
        <p class="text-2xl">Цена: €50</p>
        <div class="text-xl">
            <p>Връзки с продавача:</p>
            <p>Tel:</p>
            <p>Email:</p>
        </div>
    </div>
</div>
<br />
<div class="card">
    <h2 class="text-2xl">Описание</h2>
    <p class="text-xl">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Similique
        praesentium velit modi neque voluptates? Excepturi ut corporis magnam
        facere minus blanditiis, modi natus animi quis distinctio, placeat autem
        iste necessitatibus.
    </p>
</div>
<br />
<div class="card flex gap-2">
    <a
        class="button"
        target="_blank"
        href="https://www.landrover.bg/range-rover/overview"
        >Официален сайт на производителя</a
    >
</div>
