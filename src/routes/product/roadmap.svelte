<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import Appbar from '$lib/components/Appbar-close.svelte'
let title = 'Product roadmap'
</script>

<Appbar title="{title}"/>

<div class="grid grid-cols-1 lg:grid-cols-3 gap-8 bg-slate-100 p-8">
	<section class="p-8 bg-white">
		<h2>Product roadmap</h2>
		<ul class="p-4 list-decimal">
			<li>Create 'boards' in 'My ideaables' so that people can share boards, and see other people's boards that have been shared with them, and collaborate on it
- Instead of SaaS think about 'pay per (infrequent) transaction'. So but offering the product for free we can get user traction from ""bitches"" and uni students, founders. </li>
			<li>Integrations. Integrate to other tools (company setup, privacy policy and legal documents). Get referral commission from them.</li>
		</ul>
	</section>
	<section class="p-8 bg-white">
		<h2>Customers</h2>
		<ul class="p-4 list-decimal">
			<li>Service providers: legal documents (company setup, privacy policies)</li>
			<li>Yet to think or more customers...</li>
		</ul>
		<h2>End users</h2>
		<ul class="p-4 list-decimal">
			<li>Core users: housewives, students, founders.</li>
			<li>Supporting users: ...</li>
			<li>Yet to think or more customers...</li>
		</ul>
		<h2>Channels</h2>
		<ul class="p-4 list-decimal">
			<li>Youtubers: ThinkSchool,</li>
			<li>Bloggers/Forums: "Bitches"</li>
			<li>Supporting products: Bubble, Atlassian etc</li>
			<li>Yet to think or more channels...</li>
		</ul>
	</section>
	<section class="p-8 bg-white">
		<h2>Revenue streams</h2>
		<ul class="p-4 list-decimal">
			<li>Non-intrusive ads through Partner services. 'Help me setup a company', 'Help me with legal work out privacy policy'.</li>
			<li>Integrations and Affiliate links. Integrate to other tools (company setup, privacy policy and legal documents). Get referral commission from them.</li>
			<li>SaaS</li>
			<li>Shop/Merchandise: Games (board or digital), Cards</li>
			<li>Yet to think or more revenue sources...</li>
		</ul>
		<p class="category-label">Breakeven approaches</p>
		<ul class="p-4 list-decimal">
			<li>Place 50 ads priced at $100 per ad per month</li>
			<li>Generate 5000 referral clicks every month * $1 per click</li>
			<li>Charge 1000 customers * $5 per customer per month subscription</li>
			<li>Yet to think or more ways...</li>
		</ul>
	</section>
</div>