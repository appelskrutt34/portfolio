

<script>
  import { fade } from "svelte/transition";
  import Linkedin from "$lib/components/icons/Linkedin.svelte"
  import Twitter from "$lib/components/icons/Twitter.svelte"
  var y;
  function scrollInto(id) {
    let element = document.getElementById(id);
    window.scrollTo({ top: element.offsetTop - 70, behavior: 'smooth'});
  }
</script>

<div class="fixed w-full top-0 z-20">
        {#if y < 50}
        <div in:fade class="w-full flex justify-center">
        <div class="container font-secondary gap-6 md:gap-0 flex flex-col md:flex-row justify-between py-6 px-4">
            <div class="flex gap-8">
                <button on:click={() => {scrollInto("skills")}}>skills</button>
                <button on:click={() => {scrollInto("toolbox")}}>toolbox</button>
                <button on:click={() => {scrollInto("history")}}>history</button>
            </div>
            <div class="flex gap-4">
                <a href="#"><Linkedin color="#fafafa"></Linkedin></a>
                <a href="#"><Twitter color="#fafafa"></Twitter></a>
            </div>
        </div>
        </div>
        {:else}
        <div in:fade class="w-full flex justify-center bg-neutral-50">
            <div class="container font-secondary gap-6 md:gap-0 flex flex-col md:flex-row justify-between py-6 px-4 text-neutral-900">
                <div class="flex gap-8">
                    <button on:click={() => {scrollInto("skills")}}>skills</button>
                    <button on:click={() => {scrollInto("toolbox")}}>toolbox</button>
                    <button on:click={() => {scrollInto("history")}}>history</button>
                </div>
                <div class="flex gap-4">
                    <a href="#"><Linkedin color="#171717"></Linkedin></a>
                    <a href="#"><Twitter color="#171717"></Twitter></a>
                </div>
            </div>
        </div>
    {/if}

</div>

<svelte:window bind:scrollY={y} />