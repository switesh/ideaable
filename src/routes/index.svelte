<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
let title = 'Sail'
</script>

<div class="px-4 py-2 flex justify-between items-center border-b border-slate-200">
  <h1 class="text-lg font-semibold">{title}</h1>
  <section>
    <a href="roadmap" class="btn">Roadmap</a>
  </section>
</div>

<section class="p-8 flex flex-col gap-4">
<h1>{title}</h1>

<section>
Your data is yours.
</section>

<section>
Free to use. Forever.
</section>
</section>

<section class="p-8 flex flex-col gap-4">
<h2>FAQ</h2>
<details>
    <summary>Why is it free?</summary>
    <p>Because the free base product helps us gain users.</p>
</details>
<details>
    <summary>What about profitablility?</summary>
    <p>By the following means</p>
    <ul>
    <li>Paid features (such as multi-user, online version etc...)</li>
    <li>Advertising. Sponsors.</li>
    </ul>
    <p>By doing so we can remain a viable business.</p>
</details>
<details>
    <summary>Our guiding principles</summary>
    <ul class="list-disc pl-4">
      <li>
        <p>Be transparent.</p>
        <p><small>Our business model is explained above, and our <a href="/">product roadmap is public ↗</a>.</small></p>
        <p><small>No VC money, no pressure, no perverse incentives.</small></p>
      </li>
      <li>
        <p>Communicate directly, without jargon or asterisks.</p>
        <p><small>It's just you and us; one-to-one relationship.</small></p>
        <p><small>We don't have sales or marketing department.</small></p>
      </li>
      <li>
        <p>No cheerleaders, no dramas.</p>
        <p><small>We don't have HR or PR department.</small></p>
        <p><small>We prefer to retain our focus on our product and you; rather than squander it on Facebook, Twitter or other attention seeking distractions.</small></p>
      </li>
      <li>
        <p>Win-win outcome.</p>
        <p><small>You - our users and customers, our staff, and our partners.</small></p>
      </li>
    </ul>
</details>
</section>

<footer class="p-8 bg-slate-600 text-slate-300">
<p>Email us at <a href="mailto:support@sail.com?subject=Product inquiry">support@sail.com</a>, or call us on <a href="tel:+4733378901">+61 0491 570 156</a></p>
</footer>
<hr class="my-8">
<footer class="p-8 bg-slate-600 text-slate-300">
<ul class="space-y-2">
  <li><a href="roadmap">Product roadmap</a></li>
  <li><a href="styleguide">Styleguide</a></li>
</ul>
</footer>

