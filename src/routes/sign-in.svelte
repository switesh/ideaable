<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'Sign in'
</script>

<Appbar/>


<section class="p-8 lg:p-16">
  <p>Sign in</p>
</section>

<Footer/>

