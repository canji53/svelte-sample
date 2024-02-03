<script lang="ts">
    export let flag: number;

    const returnStart = () => {
        flag = 0;
    }
</script>

<div class="border border-black h-[500px] rounded flex justify-center items-center flex-col">
    <h2 class="text-7xl mb-3">
        3問正解
    </h2>
    <button
        type="button"
        on:click={returnStart}
        class="bg-orange-500 py-2 px-4 rounded"
    >
        初めにもどる
    </button>
</div>
