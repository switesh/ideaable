<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'Business plan summary'
</script>

<Appbar/>

<div class="py-4 px-16 flex gap-4 justify-between items-center">
  <h1>ideaable platform</h1>
  <div class="flex gap-x-4">
    <button class="btn base">Edit</button>
  </div>
</div>
<div class="p-4 lg:p-8 lg:px-16 flex flex-col gap-4 bg-slate-100">
  <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 ">
    <section class="p-4 bg-white rounded shadow-sm">
      <p class="category-label text-lg mb-2">Business</p>
      <p><strong>What</strong> is the business about? Describe in less than 3 short sentences.</p>
      <hr class="my-2 opacity-50">
        <div class="flex flex-wrap gap-x-4 gap-y-2">
          <p class="px-1 rounded text-xs text-indigo-500 bg-indigo-50">Solve own problems</p>
          <p class="px-1 rounded text-xs text-indigo-500 bg-indigo-50">Just 1% of a very large market</p>
        </div>
    </section>
    <section class="p-4 bg-white rounded shadow-sm">
      <p class="category-label text-lg mb-2">Customers</p>
      <p><strong>Who</strong> are the customers (customer segments)?</p>
      <p class="text-sm text-slate-500 mt-2">End users use the product or service. Customers PAY for the product or service.</p>
    </section>
    <section class="p-4 bg-white rounded shadow-sm">
      <p class="category-label text-lg mb-2">Revenue streams</p>
      <p><strong>How</strong> will the business generate money? In how many different ways?</p>
      <hr class="my-2 opacity-50">
        <div class="flex flex-wrap gap-x-4 gap-y-2">
          <p class="px-1 rounded text-xs text-indigo-500 bg-indigo-50">Freemium</p>
          <p class="px-1 rounded text-xs text-indigo-500 bg-indigo-50">Micro transactions</p>
          <p class="px-1 rounded text-xs text-indigo-500 bg-indigo-50">Affiliate commissions</p>
        </div>
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
      <hr class="my-4 opacity-50">
      <p><strong>How</strong> many paying customers would you need to breakeven?</p>
      <p class="text-sm text-slate-500 mt-2">Number of customers * price per unit</p>
    </section>
  </div>
  <div class="grid grid-cols-1 gap-4 bg-slate-100">
    <section class="p-4 bg-white rounded shadow-sm">
      <p class="category-label text-lg mb-2">Competitors</p>
      <p><strong>Who</strong> are the competitors?</p>
    </section>
  </div>
</div>


<Footer/>