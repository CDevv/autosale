<script lang="ts">
    let { hidden } = $props();

    let val: number = 5000;
    const maxVal: number = 10000;

    let numInput: HTMLInputElement;
    let rangeInput: HTMLInputElement;

    function onRangeChange(event: any) {
        val = event.target.value;
        console.log(event.target.value);
        numInput.value = val.toString();
    }

    function onNumChange(event: any) {
        val = event.target.value;
        rangeInput.value = val.toString();
    }
</script>

<div {hidden}>
    <div class="card mb-4">
        <div class="form-item">
            <label for="name" class="text-xl">Модел</label>
            <input name="name" class="card p-0.5" />
        </div>
        <br />
        <div class="form-item">
            <label for="budget" class="text-xl">Бюджет</label>
            <div class="flex flex-row gap-2">
                <input
                    bind:this={rangeInput}
                    name="budget"
                    class="card p-0.5 grow"
                    type="range"
                    max={maxVal}
                    value={val}
                    oninput={onRangeChange}
                />
                <input
                    bind:this={numInput}
                    class="card p-0.5"
                    type="number"
                    max={maxVal}
                    onchange={onNumChange}
                    value={val}
                />
            </div>
        </div>
        <br />
        <div class="form-item">
            <input class="button" type="submit" value="Търсене" />
        </div>
    </div>
</div>
