<script>
  import cam01BIG from '../assets/img/VIC_ANG_CAM01_1980x1080.jpg';
  import cam02square from '../assets/img/VIC_ANG_CAM02_900x900.jpg';
  import cam01vertical from '../assets/img/VIC_ANG_CAM01_750x1334.jpg';
  import cam04vertical from '../assets/img/VIC_ANG_CAM04_750x1334.png';
  import cam05vertical from '../assets/img/VIC_ANG_CAM05_750x1334.png';
  import arrowDownBlack from '../assets/icons/arrow-down-black.svg';

  import CRB09 from '$/assets/img/CRB_B_09.jpg';
  import CRB08 from '$/assets/img/CRB_B_08.jpg';

  import pink04 from '$/assets/img/PNK04_2K.jpg';
  import pink05 from '$/assets/img/PNK05_2K.jpg';
  import { onMount } from 'svelte';

  let innerHeight = 0;
  function scroll() {
    var reveals = document.querySelectorAll('.reveal');
    for (var i = 0; i < reveals.length; i++) {
      var windowHeight = innerHeight;
      var elementTop = reveals[i].getBoundingClientRect().top;
      var elementVisible = 100;

      if (elementTop < windowHeight - elementVisible) {
        reveals[i].classList.add('active');
      } else {
        reveals[i].classList.remove('active');
      }
    }
  }

  onMount(() => scroll());
</script>

<svelte:window bind:innerHeight on:scroll={scroll} />

<section id="works" class="min-h-screen bg-white overflow-hidden">
  <div class="p-10 pb-16 flex flex-col gap-10">
    <div class="grid grid-cols-3">
      <h2 class="text-5xl font-medium col-span-2 reveal fade-left">
        Selected Works
      </h2>
      <div class="reveal fade-right">
        <img src={arrowDownBlack} alt="arrow-down-icon" />
      </div>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <img class="md:col-span-2 reveal fade-left" src={CRB09} alt="Imagen 1" />
      <div class="reveal fade-right">
        <img class="pb-4" src={CRB08} alt="Imagen 1" />
        <p>
          This was essential as we learned and experimented with ourselves, and
          subsequently what we offered as a service as we learned and
          experimented with ourselves, and subsequently what we offered as a
          service as we learned and experimented with ourselves — the ending
          result is Driftime®.
        </p>
      </div>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 reveal fade-bottom">
      <img src={cam01vertical} alt="cam1" />
      <div>
        <img src={cam04vertical} alt="cam4" />
        <p class="text-xl font-medium">VOGUE RUSSIA</p>
      </div>
      <div>
        <img src={cam05vertical} alt="cam5" />
        <div class="flex text-xl font-medium">
          <p class="grow">VOGUE</p>
          <p>©01.2021</p>
        </div>
      </div>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <div>
        <img src={pink04} alt="img2" class="reveal fade-left" />
        <p class="font-light reveal fade-bottom">
          And subsequently what we offered as a service as we learned and
          experimented with ourselves — the ending result is Driftime®.
        </p>
      </div>
      <div class="md:col-span-2">
        <img src={pink05} alt="img1" class="reveal fade-right" />
        <div class="grid grid-cols-3 reveal fade-bottom">
          <p>PINK MAMA.</p>
          <p class="text-center">PNK</p>
          <p class="text-right">©02.2021</p>
        </div>
      </div>
    </div>
  </div>
</section>
