<script lang="ts">
    import GameOver from "../components/Game/GameOver.svelte";
    import GameStart from "../components/Game/GameStart.svelte";
    import GameJudge from "../components/Game/GameJudge.svelte";
    // import Correct from "../components/Game/Correct.svelte";
    // import InCorrect from "../components/Game/InCorrect.svelte";
    import Quiz from "../components/Game/Quiz.svelte";

    let flag: number = 0;
</script>

<main>
    <div class="container h-screen-60 flex justify-center flex-col mx-auto">
        <div class="grid grid-cols-10">
            <div class="col-start-3 col-span-7">
                {#if flag === 0}
                    <GameStart bind:flag={flag} />
                {:else if flag === 1}
                    <Quiz bind:flag={flag} />
                {:else if flag === 2}
                    <GameJudge bind:flag={flag} />
                <!-- {:else if flag === 2}
                    <Correct flag={flag} />
                {:else if flag === 3}
                    <InCorrect flag={flag} /> -->
                {:else if flag === 4}
                    <GameOver bind:flag={flag} />
                {/if}
            </div>
        </div>
    </div>
</main>

<style>
    .h-screen-60 {
        height: calc(100vh - 120px);
    }
</style>
