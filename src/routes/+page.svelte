<script>
  import { onMount } from 'svelte';
  import { fade, fly, scale } from 'svelte/transition';
  import { linear, quintInOut } from 'svelte/easing';
  import SlidingLeft from "$lib/SlidingLeft.svelte";
  import SlidingRight from "$lib/SlidingRight.svelte";
  import {Linkedin} from 'lucide-svelte';


  let isLoading = true;

  function checkImagesLoaded() {
    const images = document.querySelectorAll('img');
    const totalImages = images.length;
    let loadedImages = 0;

    images.forEach((img) => {
      if (img.complete) {
        loadedImages++;
      } else {
        img.addEventListener('load', () => {
          loadedImages++;
          if (loadedImages === totalImages) {
            setTimeout(() => {
              isLoading = false;
            }, 250);
          }
        });
      }
    });

    if (loadedImages === totalImages) {
      setTimeout(() => {
        isLoading = false;
      }, 250);
    }
  }

  onMount(() => {
    checkImagesLoaded();
  });
</script>



<div class={`h-screen bg-stone-900 flex flex-col place-items-center py-4 overflow-hidden ${isLoading ? "opcaity-0" : "opacity-100"}`}>
  <SlidingLeft/>
  <div class="w-screen grid grid-cols-3 place-items-center text-stone-100 h-[24vh] relative">
    <a href="/gallery" in:fly={{ delay: 750, duration: 1400, x: -100, y: 0, easing: quintInOut }} class="text-2xl uppercase">Gallery</a>
    <div in:scale={{ delay: 100, duration: 1400, easing: quintInOut }} class="text-7xl text-center pb-2"><span class="font-semibold mr-1">Stefka</span><span class="">Bonev</span></div>
    <a href="/resume" in:fly={{ delay: 750, duration: 1400, x: 100, y: 0, easing: quintInOut }} class="text-2xl uppercase">Resume</a>
    <a target="_blank" href="https://www.linkedin.com/in/stefkaboneva/" class="absolute right-4 bottom-4 bg-blue-500 hover:bg-blue-600 p-1 rounded-md transition-all duration-500 ease-in-out hover:scale-105">
      <Linkedin size=24/>
    </a>
  </div>
  <SlidingRight/>
</div>

{#if isLoading}
  <div out:fade class="fixed top-0 left-0 w-full h-full bg-stone-900 flex place-items-center justify-center z-[9999]">
    <p class="text-white text-2xl">Loading...</p>
  </div>
{/if}
