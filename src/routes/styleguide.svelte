<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-close.svelte'
let title = 'Styleguide'
</script>

<Appbar title="{title}"/>

<div class="p-8 flex flex-col gap-4">
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>
  <p>Paragraph</p>
  <small>Small</small>
  <button class="btn-base">Button</button>
  <div class="input-wrapper">
    <label for="abc">Input label</label>
    <input type="text" name="abc">
  </div>
  <div class="input-wrapper">
    <label for="input02" class="hidden">Search</label>
    <input type="search" name="input02" class="rounded" placeholder="Search">
  </div>
  <p>Something</p>
</div>