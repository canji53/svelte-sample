<script lang="ts">
    export let flag: number;

    let answer: string = "";

    const handleSubmit = () => {
        if (answer) {
            if (answer == "ほうもん") {
                flag = 2;
            } else {
                flag = 3;
            }
        } else {
            alert('入力されていません。')
        }
    };
</script>

<div class="border border-black h-[500px] rounded flex justify-center items-center flex-col">
    <div class="text-center mb-2">
        <p class="text-3xl">
            ⚪︎⚪︎⚪︎⚪︎
        </p>
        <h2 class="text-7xl mb-3">
            訪問
        </h2>
    </div>

    <div class="mb-5">
        <input
            type="text"
            bind:value={answer}
            class="border border-black focus:outline-none rounded py-1 px-2"
        />
    </div>

    <button
        type="button"
        on:click={handleSubmit}
        class="bg-orange-400 px-5 py-2 rounded"
    >
        確定
    </button>
</div>
