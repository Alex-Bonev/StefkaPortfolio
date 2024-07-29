<script>

  import {House} from "lucide-svelte"
import img1 from "$lib/artImages/img1.jpg";import img2 from "$lib/artImages/img2.jpg";import img3 from "$lib/artImages/img3.jpg";import img4 from "$lib/artImages/img4.jpg";import img5 from "$lib/artImages/img5.jpg";
import img6 from "$lib/artImages/img6.jpg";import img7 from "$lib/artImages/img7.jpg";import img8 from "$lib/artImages/img8.jpg";import img9 from "$lib/artImages/img9.jpg";import img10 from "$lib/artImages/img10.jpg";
import img11 from "$lib/artImages/img11.jpg";import img12 from "$lib/artImages/img12.jpg";import img13 from "$lib/artImages/img13.jpg";import img14 from "$lib/artImages/img14.jpg";import img15 from "$lib/artImages/img15.jpg";
import img16 from "$lib/artImages/img16.jpg";import img17 from "$lib/artImages/img17.jpg";import img18 from "$lib/artImages/img18.jpg";import img19 from "$lib/artImages/img19.jpg";import img20 from "$lib/artImages/img20.jpg";
import img21 from "$lib/artImages/img21.jpg";import img22 from "$lib/artImages/img22.jpg";import img23 from "$lib/artImages/img23.jpg";import img24 from "$lib/artImages/img24.jpg";import img25 from "$lib/artImages/img25.jpg";

import gmk1 from "$lib/genmarkImages/img1.jpg";import gmk2 from "$lib/genmarkImages/img2.jpg";import gmk3 from "$lib/genmarkImages/img3.jpg";import gmk4 from "$lib/genmarkImages/img4.jpg";import gmk5 from "$lib/genmarkImages/img5.jpg";
import gmk6 from "$lib/genmarkImages/img6.jpg";import gmk7 from "$lib/genmarkImages/img7.jpg";import gmk8 from "$lib/genmarkImages/img8.jpg";import gmk9 from "$lib/genmarkImages/img9.jpg";import gmk10 from "$lib/genmarkImages/img10.jpg";
import gmk11 from "$lib/genmarkImages/img11.jpg";import gmk12 from "$lib/genmarkImages/img12.jpg";import gmk13 from "$lib/genmarkImages/img13.jpg";import gmk14 from "$lib/genmarkImages/img14.jpg";import gmk15 from "$lib/genmarkImages/img15.jpg";
import gmk16 from "$lib/genmarkImages/img16.jpg";import gmk17 from "$lib/genmarkImages/img17.jpg";import gmk18 from "$lib/genmarkImages/img18.jpg";import gmk19 from "$lib/genmarkImages/img19.jpg";import gmk20 from "$lib/genmarkImages/img20.jpg";
import gmk21 from "$lib/genmarkImages/img21.jpg";import gmk22 from "$lib/genmarkImages/img22.jpg";import gmk23 from "$lib/genmarkImages/img23.jpg";

const imports = [
  img17, gmk2, img1, img10, gmk8, img19, img4, gmk13, img14, img8,
  gmk5, img6, gmk18, gmk21, img21, gmk1, img15, gmk14, img7, gmk20, img3,
  gmk6, img18, img11, gmk19, img9, gmk15, img2, img22, gmk4, img24,
  gmk23, img16, gmk7, gmk3, img12, gmk11, img5, gmk17, img13, img20, gmk10,
  img25, gmk9, img23, gmk12, gmk16, gmk22
];


</script>

<main class="w-screen bg-stone-900 flex flex-col gap-4 place-items-center">
  <div class="h-[5vh] border-stone-100 border-b-2 text-stone-100 w-full flex place-items-center py-8">
    <a href="/" class="text-center h-24 w-24 grid place-items-center text-xl z-[999]">
      <div><House size=32/></div>
    </a>
    <div class="flex-1 text-center text-4xl -ml-24">
      Gallery
    </div>
  </div>

  <div class="flex-grow flex flex-wrap gap-4 w-[95vw] place-items-center">
    {#each imports as work, i}
      <img class="h-96" alt="gallery work" src={work}/>
    {/each}
  </div>

</main>