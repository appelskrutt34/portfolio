<script>
    export let title ="";
    export let description = "";
    export let height = "h-56";
    export let width = "w-full";
</script>

<div class={"bg-lime-600 text-neutral-900 rounded-2xl p-6 relative overflow-clip " + height + " " + width}>
    <div class="absolute top-0 left-0 w-full h-full z-10 p-6">
        <div class="flex gap-4 items-center ">
            <slot name="icon"></slot>
            <h2 class="font-secondary">{title}</h2>
        </div>
        <p class="mt-8">{description}</p>
    </div>
    <slot name="image"></slot> 
</div>

