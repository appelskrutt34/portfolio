

<script>
  import { fade, slide } from "svelte/transition";
  import Linkedin from "$lib/components/icons/Linkedin.svelte"
  import Github from "$lib/components/icons/Github.svelte"
  import Twitch from "$lib/components/icons/Twitch.svelte"
  import Twitter from "$lib/components/icons/Twitter.svelte"
  import Menu from "$lib/components/icons/Menu.svelte"
  import Close from "$lib/components/icons/Close.svelte"

  var y = 0;
  var openMenu = false;

  function scrollInto(id) {
    let element = document.getElementById(id);
    window.scrollTo({ top: element.offsetTop - 100, behavior: 'smooth'});
  }
</script>

<a href="#main" class="opacity-0" aria-label="Skip to main content"></a>
<header class="fixed w-full top-0 z-20"> 
        {#if y < 50}
         <!-- Monitor -->
        <div in:fade class="w-full justify-center hidden md:flex">
            <nav class="container font-secondary gap-6 md:gap-0 flex flex-col md:flex-row justify-between py-6 px-4" aria-label="Main navigation">
                <div class="flex gap-8">
                    <button on:click={() => {scrollInto("skills")}}>skills</button>
                    <button on:click={() => {scrollInto("toolbox")}}>toolbox</button>
                    <button on:click={() => {scrollInto("history")}}>history</button>
                    <button on:click={() => {scrollInto("projects")}}>hobby projects</button>
                </div>
                <div class="flex gap-4">
                    <a href="https://www.linkedin.com" aria-label="Linkedin"><Linkedin color="#fafafa"></Linkedin></a>
                    <a href="https://github.com" aria-label="Github"><Github color="#fafafa"></Github></a>
                    <a href="https://www.twitch.tv" aria-label="Twitch"><Twitch color="#fafafa"></Twitch></a>
                    <a href="https://www.Twitter.com" aria-label="Twitter"><Twitter color="#fafafa"></Twitter></a>
                </div>
            </nav>
        </div>
        <!-- Mobile -->
        <nav in:fade class="md:hidden w-full border-b border-neutral-50" aria-label="Main mobile navigation">
            <div class="container flex justify-between py-6 px-4">
            <div class="flex gap-6">
                <a href="https://www.linkedin.com" aria-label="Linkedin"><Linkedin color="#fafafa"></Linkedin></a>
                <a href="https://github.com" aria-label="Github"><Github color="#fafafa"></Github></a>
                <a href="https://www.twitch.tv" aria-label="twitch"><Twitch color="#fafafa"></Twitch></a>
                <a href="https://www.Twitter.com" aria-label="Twitter"><Twitter color="#fafafa"></Twitter></a>
            </div>
              <button
                aria-label="Toggle main menu"
                on:click={() => {
                  openMenu = !openMenu;
                }}
              >
                {#if openMenu} <Close color="#fafafa"/> {:else} <Menu color="#fafafa"/> {/if}
              </button>
            </div>
            {#if openMenu}
              <div
                in:slide={{ y: -10, duration: 300 }}
                out:slide={{ y: -10, duration: 300 }}
                class="w-full text-center pb-4 flex flex-col gap-4 border-b border-stone-900"
                style="margin-top: -1px"
              >
              <button on:click={() => {openMenu = false; scrollInto("skills")}}>skills</button>
              <button on:click={() => {openMenu = false; scrollInto("toolbox")}}>toolbox</button>
              <button on:click={() => {openMenu = false; scrollInto("history")}}>history</button>
              <button on:click={() => {openMenu = false; scrollInto("projects")}}>hobby projects</button>
              </div>
            {/if}
        </nav>
        {:else}
        <!-- Monitor -->
        <div in:fade class="w-full justify-center bg-neutral-50 hidden md:flex">
            <nav class="container font-secondary gap-6 md:gap-0 flex flex-col md:flex-row justify-between py-6 px-4 text-neutral-900" aria-label="Main navigation">
                <div class="flex gap-8">
                    <button on:click={() => {scrollInto("skills")}}>skills</button>
                    <button on:click={() => {scrollInto("toolbox")}}>toolbox</button>
                    <button on:click={() => {scrollInto("history")}}>history</button>
                    <button on:click={() => {scrollInto("projects")}}>hobby projects</button>
                </div>
                <div class="flex gap-4">
                    <a href="https://www.linkedin.com" aria-label="Linkedin"><Linkedin color="#171717"></Linkedin></a>
                    <a href="https://github.com" aria-label="Github"><Github color="#171717"></Github></a>
                    <a href="https://www.twitch.tv/" aria-label="Twitch"><Twitch color="#171717"></Twitch></a>
                    <a href="https://www.Twitter.com" aria-label="Twitter"><Twitter color="#171717"></Twitter></a>
                </div>
            </nav>
        </div>
        <!-- Mobile -->
        <nav in:fade class="md:hidden w-full  bg-neutral-50 text-neutral-900" aria-label="Main mobile navigation">
            <div class="container flex justify-between py-6 px-4">
                <div class="flex gap-6">
                    <a href="https://www.linkedin.com/" aria-label="Linkedin"><Linkedin color="#171717"></Linkedin></a>
                    <a href="https://github.com/" aria-label="Github"><Github color="#171717"></Github></a>
                    <a href="https://www.twitch.tv" aria-label="Twitch"><Twitch color="#171717"></Twitch></a>
                    <a href="https://www.Twitter.com" aria-label="Twitter"><Twitter color="#171717"></Twitter></a>
                </div>
              <button
                aria-label="Toggle main menu"
                on:click={() => {
                  openMenu = !openMenu;
                }}
              >
                {#if openMenu} <Close color="#171717"/> {:else} <Menu color="#171717"/> {/if}
              </button>
            </div>
            {#if openMenu}
              <div
                in:slide={{ y: -10, duration: 300 }}
                out:slide={{ y: -10, duration: 300 }}
                class="w-full text-center pb-4 flex flex-col gap-4 border-b border-stone-900"
                style="margin-top: -1px"
              >
              <button on:click={() => {openMenu = false; scrollInto("skills")}}>skills</button>
              <button on:click={() => {openMenu = false; scrollInto("toolbox")}}>toolbox</button>
              <button on:click={() => {openMenu = false; scrollInto("history")}}>history</button>
              <button on:click={() => {openMenu = false; scrollInto("projects")}}>hobby projects</button>
              </div>
            {/if}
        </nav>
    {/if}
</header>

<svelte:window bind:scrollY={y} />