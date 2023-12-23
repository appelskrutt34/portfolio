<script>
    export let title = "Njord.RS"
    export let description = "Role: Svelte developer"
    export let image = "/pages/njord.png"
    export let source = "https://www.Njord.rs"
</script>

<div>
    <p class="text-lg mb-1 font-bold">{title}</p>
    <p class="mb-4">{description}</p>
    <a href={source}>
        <img src={image} alt="" class="h-[400px] w-[480px] object-cover border border-neutral-950 rounded-lg">
    </a>
</div>
