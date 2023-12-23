<script>
    export let title = "";
    export let date = "";
    export let tasks = [""];
    export let stack = "";
</script>


<div class="text-left">
    <h2 class="font-bold">{title}</h2>
    <p class="opacity-50 text-sm">{date}</p>
    <ul class="mt-4 mb-1">
        {#each tasks as task}
        <li>{task}</li>
        {/each}
    </ul>
    <p class="text-lime-600 text-sm font-secondary">{stack}</p>
</div>