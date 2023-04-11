<script lang="ts">
  import { page } from '$app/stores'
	import { Avatar } from '@skeletonlabs/skeleton';
</script>

<svelte:head>
	<title>Consultant {$page.params.slug}</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="p-10 space-4 grid-cols-1 gap-4 md:grid grid-cols-2 gap-2">
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
</div>
