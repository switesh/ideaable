<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
import businessIdeas from '$lib/data/business-ideas.json';
let title = 'Business ideas'
</script>

<Appbar/>

<section class=" ">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>Business ideas</h1>
    <div class="flex gap-x-4">
      <input type="search" placeholder="Search business ideas">
      <button class="btn base">Suggest one for me</button>
    </div>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each businessIdeas as { title, description, examples }, index}
      <article aria-posinset={index + 1} aria-setsize={businessIdeas.length} class="p-8 bg-white shadow-sm rounded flex flex-col gap-4">
        <div class="flex justify-between">
          <h2 class="font-semibold">{title}</h2>
        </div>
        <p>{description}</p>
        <p class="text-sm text-slate-400 mt-auto">{examples}</p>
      </article>
    {/each}
  </div>
  
</section>

<Footer/>