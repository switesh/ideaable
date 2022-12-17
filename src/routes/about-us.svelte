<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'About us'
</script>

<Appbar/>


<section class="">
  <div class="py-4 px-16 flex gap-4 justify-between items-center">
    <h1>About us</h1>
  </div>
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-x-16 bg-slate-100 p-16 mt-8">
    <div class="p-8 flex gap-x-8 bg-white rounded shadow-sm">
      <div class="h-20 w-20 bg-slate-200 rounded-full flex-shrink-0"></div>
      <div class="space-y-2">
        <h2 class="font-semibold">Daxesh Vadgama</h2>
        <p>Designer and Front-end developer. <br> Tech and business enthusiast.</p>
      </div>
    </div>
      <div class="p-8 flex gap-x-8 bg-white rounded shadow-sm">
      <div class="h-20 w-20 bg-slate-200 rounded-full flex-shrink-0"></div>
      <div class="space-y-2">
        <h2 class="font-semibold">Switesh Patel</h2>
        <p>UX/UI Designer. <br> Investing and business enthusiast.</p>
      </div>
    </div>
  </div>
  
  <section class="p-8 lg:p-16 mb-16">
    <h2 class="mb-4">We created this platform to solve our own problem</h2>
    <p>Write a brief story about it...</p>
  </section>

</section>

<Footer/>

