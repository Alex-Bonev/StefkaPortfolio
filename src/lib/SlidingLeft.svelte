<script>

  import gmk1 from "$lib/genmarkImages/img1.jpg"; import gmk2 from "$lib/genmarkImages/img2.jpg"; import gmk3 from "$lib/genmarkImages/img3.jpg"; import gmk4 from "$lib/genmarkImages/img4.jpg"; 
  import gmk6 from "$lib/genmarkImages/img6.jpg"; import gmk7 from "$lib/genmarkImages/img7.jpg"; import gmk9 from "$lib/genmarkImages/img9.jpg";
  import gmk11 from "$lib/genmarkImages/img11.jpg"; import gmk12 from "$lib/genmarkImages/img12.jpg"; import gmk14 from "$lib/genmarkImages/img14.jpg"; import gmk15 from "$lib/genmarkImages/img15.jpg";
  import gmk16 from "$lib/genmarkImages/img16.jpg"; import gmk17 from "$lib/genmarkImages/img17.jpg"; import gmk20 from "$lib/genmarkImages/img20.jpg";
  import gmk21 from "$lib/genmarkImages/img21.jpg"; import gmk22 from "$lib/genmarkImages/img22.jpg"; import gmk23 from "$lib/genmarkImages/img23.jpg";

  let gmkimages = [
    gmk1, gmk2, gmk14, gmk3, gmk4,
    gmk6, gmk7, gmk15, gmk9, gmk16,
    gmk11, gmk12, gmk20, gmk17, 
    gmk21, gmk22, gmk23
  ];
</script>

<style>
  @keyframes scroll-left {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-300%);
    }
  }

  .scrolling-left {
    animation: scroll-left 40s linear infinite;
    display: flex;
    width: 100%;
  }
</style>

<div class="w-[100vw] h-[38vh] grid place-items-end">
  <div class="scrolling-left flex place-items-baseline align-bottom h-full w-full gap-2">
    {#each Array(gmkimages.length*2) as _, i}
      <img class="h-[38vh]" src="{gmkimages[i % gmkimages.length]}" alt="Genmark Designs by Stefka Boneva"/>
    {/each}
  </div>
</div>