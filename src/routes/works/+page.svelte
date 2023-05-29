<script>
  import arrowDownWhite from '$/assets/icons/arrow-down-white.svg';
  import plus from '$/assets/icons/plus.svg';
  import { works } from '$/data/works';
</script>

<main>
  <section class="bg-black pt-72 pb-24 min-h-screen px-12 text-white">
    <div class="flex mb-2">
      <h2 class="grow text-5xl">All Works</h2>
      <img src={arrowDownWhite} alt="arrow-white-down" />
    </div>
    <div class="grid grid-cols-3 gap-4">
      {#each works as work (work.id)}
        <div>
          <div class="relative work-image hover:cursor-pointer">
            <img
              class="transition-all duration-500"
              src={work.img}
              alt="img1"
            />
            <div
              class="opacity-0 p-4 absolute top-0 transition-opacity delay-200 duration-300 flex w-full"
            >
              <p class="grow">VIEW MORE</p>
              <img src={plus} alt="arrow1" />
            </div>
          </div>
          <div class="flex">
            <p class="grow">{work.title}</p>
            <p>{work.date}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>
</main>

<style>
  .work-image:hover > .opacity-0 {
    opacity: 100;
  }
  .work-image:hover > img {
    @apply blur-sm;
  }
  .work-image > div > img {
    @apply rotate-0 transition-all duration-500 ease-out;
  }
  .work-image > div > img:hover {
    @apply rotate-180;
  }
</style>
