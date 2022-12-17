<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-signed-in.svelte'
import Footer from '$lib/components/Footer.svelte'
import myIdeas from '$lib/data/my-ideas.json';
import X from '$lib/components/icons/x.svelte'
let title = 'Home'
</script>

<Appbar/>

<section class="">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>My ideas</h1>
    <div class="flex gap-x-4">
      <a href="new-idea" class="btn base primary">+ New idea</a>
    </div>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each myIdeas as { title, description, url }, index}
      <button aria-posinset={index + 1} aria-setsize={myIdeas.length} class="p-8 bg-white shadow-sm rounded flex flex-col gap-4 text-left" on:click={()=>ideaDetailsDialog.showModal()}>
        <div class="flex justify-between">
          <h2>{title}</h2>
        </div>
        <p>{description}</p>
      </button>
    {/each}
  </div>
</section>

<dialog id="ideaDetailsDialog" class="absolute top-0 right-0 w-full max-w-screen-md h-full overflow-auto">
  <div class="flex justify-between">
    <h1>Improve UX on old products</h1>
    <div class="flex gap-x-4">
      <button class="btn">Edit</button>
      <button on:click={()=>ideaDetailsDialog.close()}><X/></button>
    </div>
  </div>
  <hr class="my-4 opacity-50">
  <p>Description</p>
  <h2 class="mt-8 mb-2">What</h2>
  <p>Business...</p>
  <h2 class="mt-8 mb-2">Who</h2>
  <p>Customers...</p>
  <h2 class="mt-8 mb-2">How</h2>
  <p>Revenue models blurb...</p>
  <hr class="my-8 opacity-50">
  <p>And then we can add more about Financing, Costing, Distribution channels etc...</p>
</dialog>

<Footer/>

