<script>
    import GameJudge from "../components/Game/GameJudge.svelte";

</script>

<main>
    <div class="container h-screen-60 flex justify-center flex-col">
        <div class="grid grid-cols-10">
            <div class="col-start-3 col-span-7">
		<!-- ここでコンポーネントの切り替えを行います。-->
                <!-- <GameStart /> -->
                <!-- <GameOver /> -->
                <!-- <Quiz /> -->
                <!-- <GameJudge /> -->
            </div>
        </div>
    </div>
</main>

<style>
    .h-screen-60 {
        height: calc(100vh - 120px);
    }
</style>
