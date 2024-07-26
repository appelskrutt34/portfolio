<script>
    export let title = "";
    export let description = "";
</script>

<div class="flex flex-col  text-left">
        <div class="flex justify-center items-center border border-neutral-50 rounded-lg bg-neutral-950">
            <slot></slot>
        </div>
    <div class="bg-neutral-50 p-4 rounded-lg mt-4 text-neutral-900">
        <p class="font-bold text-left">{title}</p>
        <p class="font-secondary text-left">{description}</p>
    </div>
</div>
