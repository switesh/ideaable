<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'About us'
</script>

<Appbar/>


<section class="p-8 lg:p-16">
  <h1>About us</h1>


  <section class="p-8 lg:p-16">
    <p>How we got started (read our case study)</p>
  </section>

</section>

<Footer/>

