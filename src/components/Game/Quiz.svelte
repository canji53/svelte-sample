<script lang="ts">
    import type { quizesType } from "../../types";

    export let flag: number;
    export let count: number;
    export let quizes: quizesType[];

    let answer: string = "";

    const handleSubmit = () => {
        if (answer) {
            if (answer == quizes[0].ans) {
                flag = 2;
                count += 1;
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
            {#each Array(quizes[0].ans.length) as _, i}
                ○
            {/each}
        </p>
        <h2 class="text-7xl mb-3">
            {quizes[0].ques}
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
