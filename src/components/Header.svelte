<script>
  import { goto } from '$app/navigation';
  import { onMount } from 'svelte';
  let y = 0;
  let screenSize = 0;
  let fontSize = '1.5rem';
  function scroll() {
    if (screenSize > 768) {
      var mass = Math.max(1.5, 3.75 - 0.01 * y) + 'rem';
      fontSize = mass;
    } else {
      fontSize = '1.5rem';
    }
  }

  onMount(() => scroll());
</script>

<svelte:window
  bind:scrollY={y}
  on:scroll={scroll}
  bind:innerWidth={screenSize}
/>
<header
  class="flex gap-10 font-medium fixed w-full p-4 z-10 mix-blend-difference"
>
  <nav class="grid grid-cols-3 w-full text-xl md:text-2xl">
    <a
      style="font-size: {fontSize}"
      href="/"
      class="text-6xl text-white mix-blend-difference hover:text-gray-500 ease-linear duration-500 transition-colors"
      >ÁNGEL PÉREZ STUDIO.</a
    >
    <a
      href="/works"
      class="text-white hover:text-gray-500 ease-linear duration-500 transition-colors"
    >
      Work</a
    >
    <a
      href="#about"
      class="text-white hover:text-gray-500 ease-linear duration-500 transition-colors"
    >
      About</a
    >
  </nav>
</header>
