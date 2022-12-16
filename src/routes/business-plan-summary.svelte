<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar.svelte'
import Footer from '$lib/components/Footer.svelte'
let title = 'Business plan summary'
</script>

<Appbar/>

<button>Edit</button>

<div class="px-8 lg:px-16 py-4 space-y-8">
  <h1>Business name</h1>
  <section>
    <h2>Business description</h2>
    <p>Business description blurb...no more than 3 short sentences.</p>
  </section>
  <section>
    <h2>End-users</h2>
    <p class="text-xs text-slate-400">They use your product or service.</p>
    <p>Blurb...</p>
  </section>
  <section>
    <h2>Customers</h2>
    <p class="text-xs text-slate-400">They <strong>pay</strong> for your product or service.</p>
    <p>Blurb...</p>
  </section>
  <section>
    <h2>Business model</h2>
    <p>Blurb...</p>
  </section>
  <section>
    <h2>Sources of Revenue</h2>
    <p>Blurb...</p>
  </section>
</div>

<Footer/>