<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'Case studies'
</script>

<Appbar/>

<section class="">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>Case studies</h1>
    <div class="flex gap-x-4">
      <input type="search" placeholder="Search case studies">
    </div>
  </div>
  <div class="px-16 mb-8">
    <a href="https://businessmodelnavigator.com/companies" target="_blank">Reference: Business Model Navigator - Case studies</a>
  </div>
  <iframe src="https://businessmodelnavigator.com/companies" width="100%" height="600px">
</section>

<Footer/>

