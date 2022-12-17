<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
import businessModels from '$lib/data/business-models.json';
let title = 'Business models'
</script>

<Appbar/>

<section class=" ">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>Business models</h1>
    <div class="flex gap-x-4">
      <input type="search" placeholder="Search business models">
      <button class="btn base">Suggest one for me</button>
    </div>
  </div>
  <div class="px-16">
    <a href="https://businessmodelnavigator.com/explore" target="_blank">Reference: Business Model Navigator</a>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each businessModels as { title, description, image, caseStudy, examples }, index}
      <article aria-posinset={index + 1} aria-setsize={businessModels.length} class="p-8 bg-white shadow-sm rounded">
        <h2 class="mb-4">{title}</h2>
        <p>{description}</p>
        <p class="text-xs text-slate-400">{examples}</p>
        <hr class="opacity-75 my-4">
        <footer class="flex gap-x-4 justify-between">
          <button class="btn">+</button>
          <button class="btn">♡</button>
        </footer>
      </article>
    {/each}
  </div>
  
</section>

<Footer/>

