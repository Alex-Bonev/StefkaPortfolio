<script>
  import resumeimage1 from "$lib/resumeimages/stefkaresume1.jpg"
  import resumeimage2 from "$lib/resumeimages/stefkaresume2.jpg"

  import {House} from "lucide-svelte"


</script>

<main class="w-screen h-screen bg-stone-900 flex flex-col gap-4">
  <div class="h-[5vh] border-stone-100 border-b-2 text-stone-100 w-full flex place-items-center py-8">
    <a href="/" class="text-center h-24 w-24 grid place-items-center text-xl z-[999]">
      <div><House size=32/></div>
    </a>
    <div class="flex-1 text-center text-4xl -ml-24">
      Resume
    </div>
  </div>

  <div class="flex-grow flex justify-evenly">
    <img class="h-[90vh]" alt="page one of resume" src={resumeimage1}/>
    <img class="h-[90vh]" alt="page one of resume" src={resumeimage2}/>
  </div>

</main>