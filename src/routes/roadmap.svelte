<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-close.svelte'
let title = 'Product roadmap'
</script>

<Appbar title="{title}"/>

<div class="px-8 py-4">
<h1>Create</h1>
<ul class="p-4 list-decimal">
<li>User(s) and User Task Flow</li>
<li><a href="product/kanban">Kanban</a></li>
<li>Task list</li>
<li>Competitor research</li>
<li>UX research notes/document
<ol class="list-decimal list-inside">
<li>Take notes (text and audio with transcribe)</li>
<li>Analyse and synthesize</li>
<li>Present insights (slideshow)</li>
</ol>
<li>User journey map</li>
<li>Customer journey map</li>
<li>Service blueprint</li>
<li>Analytics? Possible (free open source library)?</li>
<li>Business Model Canvas</li>
<li>SWOT</li>
<li>Onion ring (ecosystem map)</li>
<li>Visual website/app builder with Tailwind css only? Crazy?</li>
</ul>
</div>