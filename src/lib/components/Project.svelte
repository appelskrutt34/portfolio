<script>
    export let title = "";
    export let description = "";
    export let image = "";
    export let source = "";
</script>

<div class="flex flex-col  text-left">
    <a href={source} aria-label={title}>
        <img src={image} alt="" class="w-full h-auto object-cover border border-neutral-50 rounded-lg">
    </a>

    <div class="bg-neutral-50 p-4 rounded-lg mt-4 text-neutral-900">
        <p class="font-bold text-left">{title}</p>
        <p class="font-secondary text-left">{description}</p>
    </div>
</div>
