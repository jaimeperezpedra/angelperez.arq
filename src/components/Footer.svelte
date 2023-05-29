<script>
  import arrowDiagonalWhite from '../assets/icons/arrow-diagonal-white.svg';
  import arrowRightWhite from '../assets/icons/arrow-right-white.svg';
</script>

<footer id="about" class="bg-black text-white px-8 py-4">
  <div
    class="grid grid-cols-1 md:grid-cols-3 text-lg pb-10 text-center md:text-left"
  >
    <a href="/" class="text-xl">WANT TO WORK TOGETHER?</a>
    <ul class="flex flex-col items-center py-10 md:block md:py-0">
      <li class="flex">
        <a href="https://www.instagram.com/angelperezarq/" target="_blank">
          Instagram
        </a>
        <img src={arrowDiagonalWhite} alt="arrow-diagonal-white" />
      </li>
      <li class="flex">
        <a href="https://www.behance.net/angelperezarq" target="_blank">
          Behance
        </a>
        <img src={arrowDiagonalWhite} alt="arrow-diagonal-white" />
      </li>
      <li class="flex">
        <a
          target="_blank"
          href="https://www.linkedin.com/in/%C3%A1ngel-p%C3%A9rez-pedraza-304258192/"
        >
          Linkedin
        </a>
        <img src={arrowDiagonalWhite} alt="arrow-diagonal-white" />
      </li>
      <li class="flex">
        <a href="https://www.pinterest.es/angelperezarq/" target="_blank">
          Pinterest
        </a>
        <img src={arrowDiagonalWhite} alt="arrow-diagonal-white" />
      </li>
    </ul>
    <p>
      And subsequently what we offered as a service as we learned and
      experimented with ourselves — the ending result is Driftime®.
    </p>
  </div>
  <div class="grid grid-cols-1 md:grid-cols-3">
    <a
      href="/"
      class="col-span-2 text-2xl md:text-5xl xl:text-9xl text-center md:text-left pb-10 md:pb-0 break-words"
      >info@angelperez.studio</a
    >
    <form action="" class="flex flex-col gap-4 text-xl">
      <p>JOIN OUR NEWSLETTER</p>
      <input
        class="bg-transparent border-b-2 border-white placeholder-gray-700"
        type="text"
        placeholder="Name"
      />
      <input
        class="bg-transparent border-b-2 border-white placeholder-gray-700"
        type="text"
        placeholder="Email"
      />
      <button type="submit">
        <img src={arrowRightWhite} alt="arrow-right" />
      </button>
    </form>
  </div>
</footer>
