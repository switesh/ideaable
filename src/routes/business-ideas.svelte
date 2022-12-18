<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
import businessIdeas from '$lib/data/business-ideas.json'
import X from '$lib/components/icons/x.svelte'
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
      <button aria-posinset={index + 1} aria-setsize={businessIdeas.length} class="p-8 bg-white shadow-sm rounded flex flex-col gap-4 text-left" on:click={()=>businessIdeaDetailsDialog.showModal()}>
        <div class="flex justify-between">
          <h2 class="font-semibold">{title}</h2>
        </div>
        <p>{description}</p>
        <p class="text-sm text-slate-500 mt-auto">{examples}</p>
      </button>
    {/each}
  </div>
  
</section>

<dialog id="businessIdeaDetailsDialog" class="absolute top-0 right-0 max-w-screen-lg h-full">
  <div class="px-6 py-3 flex justify-between bg-slate-50 sticky top-0">
    <h1>Business idea</h1>
    <div class="flex gap-x-4">
      <button on:click={()=>businessIdeaDetailsDialog.close()}><X/></button>
    </div>
  </div>
  <hr class="px-6 my-4 opacity-50">
  <section class="px-6 py-3">
    <p>Blurb about business idea, examples of who uses it and how to apply it etc.</p>
  </section>
</dialog>

<Footer/>