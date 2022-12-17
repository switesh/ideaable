<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'Shop'
</script>

<Appbar/>

<section class="p-8 px-16">
  <h1>Shop</h1>

  <div class="p-8 bg-white shadow-sm rounded">
    <h2 class="mb-4">Card deck</h2>
    <p>A deck of cards for business models</p>
  </div>
  <div class="p-8 bg-white shadow-sm rounded">
    <h2 class="mb-4">Board game</h2>
    <p>A board game (like monopoly) to build businesses</p>
  </div>
</section>

<Footer/>

