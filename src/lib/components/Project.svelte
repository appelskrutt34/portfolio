<script>
    export let title = "";
    export let description = "";
    export let image = "";
    export let source = "";
</script>

<div>
    <p class="text-lg mb-1 font-bold">{title}</p>
    <p class="mb-4">{description}</p>
    <a href={source}>
        <img src={image} alt="" class="h-[400px] w-[480px] object-cover border border-neutral-900 rounded-lg">
    </a>
</div>
