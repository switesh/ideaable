<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'ideaable : Business idea and model generator'
</script>

<Appbar/>

<section class="p-8 lg:p-16 flex gap-x-16 xl:gap-x-32 justify-center items-center bg-violet-50">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <p class="uppercase text-6xl text-violet-500 font-black">Overcome <br> mental blocks</p>
    <a href="sign-up" class="btn base primary w-fit">Start an idea now</a>
  </div>
</section>
<section class="p-8 lg:p-16 flex flex-row-reverse gap-x-16 xl:gap-x-32 justify-center items-center">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <h1>Where do I start?</h1>
    <a href="business-ideas" class="btn base primary w-fit">Help me find ideas</a>
  </div>
</section>
<section class="p-8 lg:p-16 flex gap-x-16 xl:gap-x-32 justify-center items-center bg-violet-50">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <h1>How do I monitize it?</h1>
    <a href="business-models" class="btn base primary w-fit">Find business models to monitize my idea</a>
  </div>
</section>
<section class="p-8 lg:p-16 flex flex-row-reverse gap-x-16 xl:gap-x-32 justify-center items-center">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <h1>Is there a market for it?</h1>
    <a href="/" class="btn base primary w-fit">Find a product-market fit</a>
  </div>
</section>
<hr class="my-8 opacity-50">
<section class="p-8 lg:p-16 flex gap-x-16 xl:gap-x-32 justify-center items-center bg-violet-50">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <h1>How we got started</h1>
    <a href="about-us" class="btn base primary w-fit">Read our case study</a>
  </div>
</section>
<section class="p-8 lg:p-16 flex flex-row-reverse gap-x-16 xl:gap-x-32 justify-center items-center">
  <div class="h-96 w-full max-w-xl bg-violet-100"></div>
  <div class="p-8 flex flex-col gap-8">
    <h1>What can I create with ideaable?</h1>
    <a href="business-plan-summary" class="btn base primary w-fit">See what the end result looks like</a>
  </div>
</section>

<Footer/>

