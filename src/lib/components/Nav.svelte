

<script>
  import { fade } from "svelte/transition";
  import Linkedin from "$lib/components/icons/Linkedin.svelte"
  import Github from "$lib/components/icons/Github.svelte"
  import Twitch from "$lib/components/icons/Twitch.svelte"
  var y = 0;
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
                <a href="https://www.linkedin.com/in/ebba-svensson-6a295b187/"><Linkedin color="#fafafa"></Linkedin></a>
                <a href="https://github.com/appelskrutt34"><Github color="#fafafa"></Github></a>
                <a href="https://www.twitch.tv/hutnelf"><Twitch color="#fafafa"></Twitch></a>
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
                    <a href="https://www.linkedin.com/in/ebba-svensson-6a295b187/"><Linkedin color="#171717"></Linkedin></a>
                    <a href="https://github.com/appelskrutt34"><Github color="#171717"></Github></a>
                    <a href="https://www.twitch.tv/hutnelf"><Twitch color="#171717"></Twitch></a>
                </div>
            </div>
        </div>
    {/if}

</div>

<svelte:window bind:scrollY={y} />