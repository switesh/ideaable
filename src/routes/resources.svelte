<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
import resources from '$lib/data/resources.json';
let title = 'Resources'
</script>

<Appbar/>

<section class=" ">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>Resources</h1>
    <div class="flex gap-x-4">
      <input type="search" placeholder="Search resources">
    </div>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each resources as { title, description, url, logo }, index}
      <article aria-posinset={index + 1} aria-setsize={resources.length} class="bg-white shadow-sm rounded">
        <a href="{url}" target="_blank" class="block p-8 no-underline">
          <div class="flex gap-4">
          <img src="{logo}" alt="{title}" class="w-8 h-8 object-contain">
            <div class="space-y-4">
              <h2>{title}</h2>
              <p>{description}</p>
            </div>
          </div>
        </a>
      </article>
    {/each}
  </div>
</section>

<Footer/>

