<script lang="ts">
  import { page } from '$app/stores'
	import { Avatar } from '@skeletonlabs/skeleton';
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	let tabSet: number = 0;
</script>

<svelte:head>
	<title>Consultant {$page.params.slug}</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="p-10 space-4 grid grid-cols-1 gap-4 md:grid grid-cols-4 gap-4">
		<div class="card p-4 col-span-4 bg-variant-filled-surface flex flex-row" style="justify-content:space-between;">
			<Avatar src="https://dnfx0kvkzsynw.cloudfront.net/websites/25/personnages/arthur.jpg" width="w-32" class="ml-10 mr-10 hidden none md:block"/>
			<div class="flex flex-col justify-center">
				<h3>Arthur Pendragon</h3>
				<h4>Roi de Bretagne</h4>
			</div>
			<div class="flex flex-col justify-center">
				<a href="/" class="btn variant-filled-primary">
					<span><svg class="h-6 w-6 text-white"  viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <path d="M9 7 h-3a2 2 0 0 0 -2 2v9a2 2 0 0 0 2 2h9a2 2 0 0 0 2 -2v-3" />  <path d="M9 15h3l8.5 -8.5a1.5 1.5 0 0 0 -3 -3l-8.5 8.5v3" />  <line x1="16" y1="5" x2="19" y2="8" /></svg></span>
					<span>Editer</span>
				</a>
			</div>
		</div>
		<div class="card p-4 col-span-4 bg-variant-filled-surface flex flex-col">
			<h2 class= "text-center">Missions</h2>
			<TabGroup>
				<Tab bind:group={tabSet} name="tab1" value={0}>Toutes les missions</Tab>
				<Tab bind:group={tabSet} name="tab2" value={1}>Missions en cours</Tab>
				<Tab bind:group={tabSet} name="tab3" value={2}>Missions terminées</Tab>
				<!-- Tab Panels --->
				<svelte:fragment slot="panel">
					{#if tabSet === 0}
			<div class="flex flex-row">
				<a class="block card card-hover p-4 m-5 variant-filled-surface w-full 2xl: w-1/2 m-1" href="#">
					<div class="flex flex-row">
						<img src="https://fr.web.img6.acsta.net/r_654_368/newsv7/20/09/07/17/09/2717008.jpg" width="w-32" class="mr-10 hidden none md:block w-32 h-32"/>
						<div class="flex flex-col justify-center">
							<h5>Roi de Bretagne par interim</h5>
							<p>Faut arrêter ces conneries de nord et de sud ! Une fois pour toutes, le nord, suivant comment on est tourné, ça change tout !</p>
							<i><bold> Jan 500 - Dec 535 </bold></i>
						</div>
					</div>
				</a>
				<a class="block card card-hover p-4 m-5 variant-filled-surface w-full 2xl: w-1/2 m-1" href="#">
					<div class="flex flex-row">
						<Avatar src="https://fr.web.img6.acsta.net/r_654_368/newsv7/20/09/07/17/09/2717008.jpg" width="w-32" class="mr-10 hidden none md:block"/>
						<div class="flex flex-col justify-center">
							<h5>Roi de Bretagne par interim</h5>
							<p>Faut arrêter ces conneries de nord et de sud ! Une fois pour toutes, le nord, suivant comment on est tourné, ça change tout !</p>
							<i><bold> Jan 500 - Dec 535 </bold></i>
						</div>
					</div>
				</a>
			</div>
					{:else if tabSet === 1}
						(tab panel 2 contents)
					{:else if tabSet === 2}
						(tab panel 3 contents)
					{/if}
				</svelte:fragment>
			</TabGroup>
		</div>
</div>
