<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-close.svelte'
let title = 'Kanban'
</script>

<Appbar title="{title}"/>

<div class="flex flex-col h-full">
<div class="p-8 bg-slate-50 flex-1 h-full">
<a href="https://flowbite.com/application-ui/demo/kanban/" target="_blank">Kanban from Flowbite</a>
</div>
</div>