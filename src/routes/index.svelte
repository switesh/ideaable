<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'ideaable : Business idea and model generator'
</script>

<Appbar/>

<section class="p-8 px-16 flex gap-x-16 xl:gap-x-32 justify-center items-center">
  <div class="h-96 w-full max-w-sm bg-slate-100"></div>
  <div class="p-8 flex flex-col gap-4">
    <p class="uppercase text-6xl text-indigo-500 font-black">Overcome <br> mental blocks</p>
    <a href="sign-up" class="btn base primary w-fit">Start an idea now</a>
  </div>
</section>

<section class="p-8 lg:p-16">
  <a href="business-plan-summary" class="btn base">See what the end result looks like</a>
</section>


<section class="p-8 lg:p-16">
  <p>How we got started (read our case study)</p>
</section>

<Footer/>

