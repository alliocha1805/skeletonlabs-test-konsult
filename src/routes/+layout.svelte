<script lang='ts'>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation/Navigation.svelte';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import { Avatar } from '@skeletonlabs/skeleton';

	function drawerOpen() 
  {
		drawerStore.open({});
	}
</script>

<!-- App Shell -->
<Drawer>
	<h2 class="p-4">Navigation</h2>
	<hr />
	<Navigation />
</Drawer>
<AppShell slotSidebarLeft="bg-surface-500/5 w-0 lg:w-64">
	<svelte:fragment slot="pageHeader">
		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
					<button class="lg:hidden btn btn-sm mr-4 " on:click={drawerOpen}>
							<span>
									<svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
											<rect width="100" height="20" />
											<rect y="30" width="100" height="20" />
											<rect y="60" width="100" height="20" />
									</svg>
							</span>
					</button>
			</svelte:fragment>
			<strong class="text-xl uppercase">Konsult.io</strong>
			
			<svelte:fragment slot="trail">
			<Avatar
				border="border-4 border-surface-300-600-token hover:!border-primary-500"
				cursor="cursor-pointer"
				initials="AP"/>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<Navigation />
	</svelte:fragment>



	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">
		<div class="bg-surface-100-800-token  space-y-4 p-4">Konsult.io TradeMark Piloy de la société Piloy</div>
	</svelte:fragment>
	<!--<svelte:fragment slot="footer">
		<div class="bg-surface-100-800-token  space-y-4 p-4">Footer Extérieur</div>
	</svelte:fragment>-->
</AppShell>
