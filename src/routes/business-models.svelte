<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
import businessModels from '$lib/data/business-models.json'
import X from '$lib/components/icons/x.svelte'
let title = 'Business models'
</script>

<Appbar/>

<section class=" ">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>{title}</h1>
    <div class="flex gap-x-4">
      <input type="search" placeholder="Search business models">
      <button class="btn base">
        <svg viewBox="0 0 24 24" width="24" height="24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1"><polygon points="22 3 2 3 10 12.46 10 19 14 21 14 12.46 22 3"></polygon></svg>
      </button>
      <button class="btn base">Suggest one for me</button>
    </div>
  </div>
  <div class="px-16">
    <a href="https://businessmodelnavigator.com/explore" target="_blank">Reference: Business Model Navigator</a>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each businessModels as { title, description, image, caseStudy, examples }, index}
      <button aria-posinset={index + 1} aria-setsize={businessModels.length} class="p-8 bg-white shadow-sm rounded flex flex-col gap-4 text-left" on:click={()=>businessModelDetailsDialog.showModal()}>
        <div class="flex justify-between w-full">
          <h2 class="font-semibold">{title}</h2>
          <div class="flex gap-x-4">
            <button class="btn p-1">+</button>
            <button class="btn p-1">♡</button>
          </div>
        </div>
        <p>{description}</p>
        <p class="text-sm text-slate-400 mt-auto">{examples}</p>
      </button>
    {/each}
  </div>
  
</section>

<dialog id="businessModelDetailsDialog" class="absolute top-0 right-0 max-w-screen-lg h-full">
  <div class="px-6 py-3 flex justify-between bg-slate-50 sticky top-0">
    <h1>Business model</h1>
    <div class="flex gap-x-4">
      <button on:click={()=>businessModelDetailsDialog.close()}><X/></button>
    </div>
  </div>
  <hr class="px-6 my-4 opacity-50">
  <section class="px-6 py-3">
    <p>Blurb about business model, examples of who uses it etc.</p>
  </section>
</dialog>

<Footer/>