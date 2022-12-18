<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-signed-in.svelte'
import Footer from '$lib/components/Footer.svelte'
import myIdeas from '$lib/data/my-ideas.json'
import X from '$lib/components/icons/x.svelte'
let title = 'Home'
</script>

<Appbar/>

<section class="">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>My ideaables</h1>
    <div class="flex gap-x-4">
      <a href="new-idea" class="btn base primary">+ New ideaable</a>
    </div>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-8 bg-slate-100 p-16 mt-8">
    {#each myIdeas as { title, description, url, revenueModel }, index}
      <button aria-posinset={index + 1} aria-setsize={myIdeas.length} class="p-8 bg-white shadow-sm rounded flex flex-col gap-4 text-left" on:click={()=>ideaDetailsDialog.showModal()}>
        <div class="flex justify-between w-full">
          <h2 class="font-semibold">{title}</h2>
        </div>
        <p>{description}</p>
        <div class="mt-auto space-y-2">
          <p class="category-label">Revenue streams</p>
          <p class="text-sm text-slate-500">{revenueModel}</p>
        </div>
      </button>
    {/each}
  </div>
</section>

<dialog id="ideaDetailsDialog" class="absolute top-0 right-0 h-full">
  <div class="px-6 py-3 flex justify-between bg-white sticky top-0">
    <h1>Gift a share</h1>
    <div class="flex gap-x-4">
      <button class="btn base"><span class="pr-2">🖉</span> Edit</button>
      <button on:click={()=>ideaDetailsDialog.close()}><X/></button>
    </div>
  </div>
  <div class="p-4 flex flex-col gap-4 bg-slate-100">
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 ">
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Business</p>
        <p><strong>What</strong> is the business about? Describe in less than 3 short sentences.</p>
      </section>
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Customers</p>
        <p><strong>Who</strong> are the customers (customer segments)?</p>
        <p class="text-sm text-slate-500 mt-2">End users use the product or service. Customers PAY for the product or service.</p>
      </section>
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Revenue streams</p>
        <p><strong>How</strong> will the business generate money? In how many different ways?</p>
      </section>
    </div>
    <div class="grid grid-cols-1 gap-4 bg-slate-100">
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Proposition</p>
        <p><strong>What</strong> aspect of this business/product/service makes it valuable to the customer?</p>
      </section>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 bg-slate-100">
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Product or service</p>
        <p class="mt-2"><strong>Who</strong> will help you make it (suppliers, partners)?</p>
        <p class="mt-2"><strong>Who</strong> will help you distribute/sell it (partners, distributors)?</p>
      </section>
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Channels</p>
        <p><strong>How</strong> will you find your customers?</p>
      </section>
      <section class="p-4 bg-white rounded shadow-sm">
        <p class="category-label text-lg mb-2">Cost structure</p>
        <p><strong>What</strong> is the cost of operating this business (Fixed and Variable, or per unit)?</p>
      </section>
    </div>
  </div>
  <hr class="px-6 my-4 opacity-50">
  <section class="px-6 py-3">
    <p>It’s the gift that keeps giving (compound interest/earnings).</p>
    <h2 class="mt-8 mb-2">What</h2>
    <p>A platform for Guardians (parents, godparents, uncles, aunts) to gift shares to Children (sons, daughters, nephews, nieces, godchildren).</p>
    <h2 class="mt-8 mb-2">Who</h2>
    <p class="category-label py-2">Immediate family</p>
    <ul class="list-decimal list-inside mb-4">
      <li>Parents</li>
      <li>Grandparents</li>
      <li>Godparents</li>
      <li>Uncles and Aunts</li>
    </ul>
    <p class="category-label py-2">Friends of family</p>
    <ul class="list-decimal list-inside">
      <li>Godparents</li>
    </ul>
    <h2 class="mt-8 mb-2">How</h2>
    <p class="category-label py-2">Business model</p>
    <ul class="list-decimal list-inside mb-4">
      <li>Offer the core product for free (or at cost for brokerage fees), but make money in surrounding areas.</li>
    </ul>
    <p class="category-label py-2">Revenue model</p>
    <ul class="list-decimal list-inside mb-4">
      <li>Negotiate bulk discount from Broker so that we may keep the discount/spread (e.g. if brokerage fees are $5 per share, but we get a $0.5 discount from broker, then we get to keep $0.5 every time a customer purchases a share).</li>
      <li>Partner up with physical gift providers.</li>
      <li>Run promos festive and celabratory seasons like birthdays, weddings</li>
    </ul>
    <hr class="my-8 opacity-50">
    <p>And then we can add more about Financing, Costing, Distribution channels etc...</p>
  </section>
</dialog>

<Footer/>

