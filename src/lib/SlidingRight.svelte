<script>

  import img1 from "$lib/artImages/img1.jpg"; import img3 from "$lib/artImages/img3.jpg"; import img4 from "$lib/artImages/img4.jpg"; import img5 from "$lib/artImages/img5.jpg";
   import img6 from "$lib/artImages/img6.jpg"; import img9 from "$lib/artImages/img9.jpg"; 
   import img12 from "$lib/artImages/img12.jpg"; import img14 from "$lib/artImages/img14.jpg"; import img15 from "$lib/artImages/img15.jpg";
   import img16 from "$lib/artImages/img16.jpg"; import img17 from "$lib/artImages/img17.jpg"; import img18 from "$lib/artImages/img18.jpg"; import img19 from "$lib/artImages/img19.jpg"; import img20 from "$lib/artImages/img20.jpg";
   import img21 from "$lib/artImages/img21.jpg"; import img22 from "$lib/artImages/img22.jpg"; import img23 from "$lib/artImages/img23.jpg"; import img24 from "$lib/artImages/img24.jpg"; import img25 from "$lib/artImages/img25.jpg"

  let artimages = [
    img1, img3, img4, img5,
    img6, img9, 
    img12, img14, img15,
    img16, img17, img18, img19, img20,
    img21, img22, img23, img24, img25
  ];

</script>

<style>
  @keyframes scroll-right {
    0% {
      transform: translateX(-300%);
    }
    100% {
      transform: translateX(0);
    }
  }

  .scrolling-right {
    animation: scroll-right 40s linear infinite;
    display: flex;
    width: 100%;
  }
</style>

<div class="w-[100vw] h-[38vh] grid place-items-start">
  <div class="scrolling-right flex place-items-start h-full gap-2">
    {#each Array(artimages.length*2) as _, i}
      <img class="h-[38vh]" src="{artimages[i % artimages.length]}" alt="Artwork by Stefka Boneva"/>
    {/each}
  </div>
</div>