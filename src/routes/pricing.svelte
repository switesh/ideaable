<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-signed-in.svelte'
import Footer from '$lib/components/Footer.svelte'
import myIdeas from '$lib/data/my-ideas.json';
import CheckmarkBullet from '$lib/components/icons/checkmarkBullet.svelte'
let title = 'Pricing'
</script>

<Appbar/>

<div class="py-4 px-16 flex gap-4 justify-between items-center">
  <h1>Pricing</h1>
</div>

<div class="my-8 w-full md:w-2/3 grid grid-cols-1 md:grid-cols-2 gap-8 mx-auto">
  <div class="shadow p-5 rounded border-t-4 border-violet-400 bg-white">
    <p class="uppercase text-sm font-medium text-slate-500">
      Starter
    </p>
    <p class="mt-4 text-3xl text-slate-700 font-medium">
      Free
    </p>
    <p class="mt-4 font-medium text-slate-700">
      Free to learn and ideate
    </p>
    <div class="mt-8">
      <ul class="grid grid-cols-1 gap-4">
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Business ideas
        </li>
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Business models
        </li>
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Case studies
        </li>
      </ul>
    </div>
    <div class="mt-8">
      <button class="btn base primary w-full">
        Try ideaable for free
      </button>
    </div>
  </div>

  <div class="shadow p-5 rounded border-t-4 border-violet-400 bg-white">
    <p class="uppercase text-sm font-medium text-slate-500">
      Standard
    </p>
    <p class="mt-4 text-3xl text-slate-700 font-medium">
      $4.99 <span class="text-base font-normal">/month</span>
    </p>
    <p class="mt-4 font-medium text-slate-700">
      All in free, plus
    </p>
    <div class="mt-8">
      <ul class="grid grid-cols-1 gap-4">
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Create your own ideaables
        </li>
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Save and monitor your ideaables
        </li>
        <li class="inline-flex">
          <CheckmarkBullet/>
          Add your own custom fields (like costing, financing, business issues etc)
        </li>
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          Collaborate, share, and export ideaables
        </li>
        <li class="inline-flex items-start">
          <CheckmarkBullet/>
          More features to come...
        </li>
      </ul>
    </div>
    <div class="mt-8">
      <button class="btn base primary w-full">
        Sign up
      </button>
    </div>
  </div>
</div>

<Footer/>