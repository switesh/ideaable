<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import { goto } from '$app/navigation';
// import Appbar from '$lib/components/Appbar-close.svelte'
import X from '$lib/components/icons/x.svelte'
let title = 'New idea'
</script>

<!-- <Appbar title="{title}"/> -->

<div class="px-4 py-2 md:px-8 md:py-4 flex justify-between items-center border-b border-slate-200">
  <h1 class="text-lg font-semibold">{title}</h1>
  <section>
    <button on:click={()=>goto('home')}><X/></button>
  </section>
</div>
<section class="p-8 lg:p-16">
  <form class="p-8 space-y-8 max-w-screen-sm mx-auto">
    <h1>What</h1>
    <p>What is your business about? What are you offering?</p>
    <div class="input-wrapper">
      <label for="business">Business description</label>
      <textarea rows="6" name="business" />
    </div>
    <a href="home" class="btn base primary block text-center">Continue ></a>
  </form>
  <form class="p-8 space-y-8 max-w-screen-sm mx-auto">
    <h1>Who</h1>
    <p>Who is/are your customer(s)? Create customer segments and categorize</p>
    <div class="input-wrapper">
      <label for="customers">Customers</label>
      <input type="text" name="customers">
    </div>
    <div class="flex gap-x-4">
      <button class="btn base">+ Add customer segment</button>
      <button class="btn base">+ Add customer</button>
    </div>
    <p>Are your end users different from your customers?</p>
    <div class="input-wrapper">
      <label for="users">End-users</label>
      <input type="text" name="users">
    </div>
    <a href="home" class="btn base primary block text-center">Continue ></a>
  </form>
  <form class="p-8 space-y-8 max-w-screen-sm mx-auto">
    <h1>How</h1>
    <p>How are you going to generate revenue?</p>
    <div class="input-wrapper">
      <label for="rev">Revenue model(s)</label>
      <input type="text" name="rev">
    </div>
    <div class="flex gap-x-4">
      <button class="btn base">+ Add revenue models</button>
      <button class="btn base">🔍 Suggest revenue models</button>
    </div>
    <a href="home" class="btn base primary block text-center">Continue ></a>
  </form>
</section>