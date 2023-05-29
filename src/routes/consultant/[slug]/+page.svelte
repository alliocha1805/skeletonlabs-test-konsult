<script lang="ts">
  import { page } from '$app/stores'
	import { Avatar } from '@skeletonlabs/skeleton';
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	import { InputChip } from '@skeletonlabs/skeleton';
	import { Autocomplete } from '@skeletonlabs/skeleton';
	import type { AutocompleteOption } from '@skeletonlabs/skeleton';
	let tabSet: number = 0;
	let inputChip = '';
	let inputChipList: string[] = ['vanilla', 'chocolate'];

	const flavorOptions: AutocompleteOption[] = [
		{ label: 'Vanilla', value: 'vanilla', keywords: 'plain, basic', meta: { healthy: false } },
		{ label: 'Chocolate', value: 'chocolate', keywords: 'dark, white', meta: { healthy: false } },
		{ label: 'Strawberry', value: 'strawberry', keywords: 'fruit', meta: { healthy: true } },
		{ label: 'Neapolitan', value: 'neapolitan', keywords: 'mix, strawberry, chocolate, vanilla', meta: { healthy: false } },
		{ label: 'Pineapple', value: 'pineapple', keywords: 'fruit', meta: { healthy: true } },
		{ label: 'Peach', value: 'peach', keywords: 'fruit', meta: { healthy: true } }
	];

function onInputChipSelect(event: any): void {
	inputDemo = event.detail.label;
}
</script>

<svelte:head>
	<title>Consultant {$page.params.slug}</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="p-10 space-4 grid grid-cols-1 gap-4 md:grid grid-cols-4 gap-4">
		<!--Bloc en tete information-->
		<div class="card p-4 col-span-4 bg-variant-filled-surface flex flex-row" style="justify-content:space-between;">
			<Avatar src="https://dnfx0kvkzsynw.cloudfront.net/websites/25/personnages/arthur.jpg" width="w-32" class="ml-10 mr-10 hidden none md:block"/>
			<div class="flex flex-col justify-center">
				<h2>Arthur Pendragon</h2>
				<h4>Roi de Bretagne</h4>
			</div>
			<div class="flex flex-col justify-center">
				<a href="/" class="btn variant-filled-primary">
					<span><svg class="h-6 w-6 text-white"  viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <path d="M9 7 h-3a2 2 0 0 0 -2 2v9a2 2 0 0 0 2 2h9a2 2 0 0 0 2 -2v-3" />  <path d="M9 15h3l8.5 -8.5a1.5 1.5 0 0 0 -3 -3l-8.5 8.5v3" />  <line x1="16" y1="5" x2="19" y2="8" /></svg></span>
					<span>Editer</span>
				</a>
			</div>
		</div>
		<!--Bloc col cote gauche-->
		<div class="flex flex-col col-span-4 md:col-span-1">
			<div class="card p-4 mb-4 bg-variant-filled-surface flex flex-col">
				<h3 class= "text-center">Informations</h3>
				<InputChip bind:input={inputChip} bind:value={inputChipList} name="chips" />
				<div class="card w-full max-w-sm max-h-48 p-4 overflow-y-auto">
					<Autocomplete
						bind:input={inputChip}
						options={flavorOptions}
						denylist={inputChipList}
						on:selection={onInputChipSelect}
					/>
				</div>
			</div>
			<div class="card p-4 bg-variant-filled-surface flex flex-col" style="justify-content:space-between;">
				<h3 class= "text-center">Skills</h3>
			</div>		
		</div>
		<!--Bloc Experiences-->
		<div class="card p-4 col-span-4 bg-variant-filled-surface md:col-span-3" style="justify-content:space-between;">
			<h3 class= "text-center">Expériences</h3>
			<div class="grid grid-cols-4">
				<div class="col-span-1">
					<Avatar src="https://www.francebleu.fr/s3/cruiser-production/2021/05/34c62b6c-b075-4b33-bbc4-1a92dedf2d77/1200x680_img_6957.jpg" width="w-32" class="ml-10 mt-10 hidden none md:block"/>
				</div>
				<div class="col-span-4 md:col-span-3">
					<div class="flex flex-col">
						<h4>Roi de Bretagne</h4>
						<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat, ante a sodales sagittis, nunc urna laoreet risus, eget pulvinar turpis dui sit amet augue. Vivamus ac volutpat nunc. Aliquam imperdiet id nulla non eleifend. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque in sagitstis erat, a accumsan lectus. Curabitur ante dolor, ultricies nec mollis ut, elementum at ipsum. Suspendisse ac nisi ut est scelerisque semper. Donec sed felis pretium, fringilla nisl sit amet, vulputate eros. Vestibulum dolor justo, rhoncus vel posuere at, mattis quis velit. Duis efficitur eleifend lectus a tristique. Donec nec venenatis elit.</p>
						<i>Jan 500 - Dec 535</i>
						<a href="/" class="btn variant-filled m-4">Detail</a>
					</div>
				</div>
				<hr class="col-span-4 mt-4 mb-4"/>
			</div>
			<div class="grid grid-cols-4">
				<div class="col-span-1">
					<Avatar src="https://www.francebleu.fr/s3/cruiser-production/2021/05/34c62b6c-b075-4b33-bbc4-1a92dedf2d77/1200x680_img_6957.jpg" width="w-32" class="ml-10 mt-10 hidden none md:block"/>
				</div>
				<div class="col-span-4 md:col-span-3">
					<div class="flex flex-col">
						<h4>Roi de Bretagne</h4>
						<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat, ante a sodales sagittis, nunc urna laoreet risus, eget pulvinar turpis dui sit amet augue. Vivamus ac volutpat nunc. Aliquam imperdiet id nulla non eleifend. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesquse in sagittis erat, a accumsan lectus. Curabitur ante dolor, ultricies nec mollis ut, elementum at ipsum. Suspendisse ac nisi ut est scelerisque semper. Donec sed felis pretium, fringilla nisl sit amet, vulputate eros. Vestibulum dolor justo, rhoncus vel posuere at, mattis quis velit. Duis efficitur eleifend lectus a tristique. Donec nec venenatis elit.</p>
						<i>Jan 500 - Dec 535</i>
						<a href="/" class="btn variant-filled">Detail</a>
					</div>
				</div>
				<hr class="col-span-4 mt-4 mb-4"/>
			</div>
			<div class="grid grid-cols-4">
				<div class="col-span-1">
					<Avatar src="https://www.francebleu.fr/s3/cruiser-production/2021/05/34c62b6c-b075-4b33-bbc4-1a92dedf2d77/1200x680_img_6957.jpg" width="w-32" class="ml-10 mt-10 hidden none md:block"/>
				</div>
				<div class="col-span-4 md:col-span-3">
					<div class="flex flex-col">
						<h4>Roi de Bretagne</h4>
						<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat, ante a sodales sagittis, nunc urna laoreet risus, eget pulvinar turpis dui sit amet augue. Vivamus ac volutpat nunc. Aliquam imperdiet id nulla non eleifend. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesquse in sagittis erat, a accumsan lectus. Curabitur ante dolor, ultricies nec mollis ut, elementum at ipsum. Suspendisse ac nisi ut est scelerisque semper. Donec sed felis pretium, fringilla nisl sit amet, vulputate eros. Vestibulum dolor justo, rhoncus vel posuere at, mattis quis velit. Duis efficitur eleifend lectus a tristique. Donec nec venenatis elit.</p>
						<i>Jan 500 - Dec 535</i>
						<a href="/" class="btn variant-filled">Detail</a>
					</div>
				</div>
				<hr class="col-span-4 mt-4 mb-4"/>
			</div>
			<div class="grid grid-cols-4">
				<div class="col-span-1">
					<Avatar src="https://www.francebleu.fr/s3/cruiser-production/2021/05/34c62b6c-b075-4b33-bbc4-1a92dedf2d77/1200x680_img_6957.jpg" width="w-32" class="ml-10 mt-10 hidden none md:block"/>
				</div>
				<div class="col-span-4 md:col-span-3">
					<div class="flex flex-col">
						<h4>Roi de Bretagne</h4>
						<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat, ante a sodales sagittis, nunc urna laoreet risus, eget pulvinar turpis dui sit amet augue. Vivamus ac volutpat nunc. Aliquam imperdiet id nulla non eleifend. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesquse in sagittis erat, a accumsan lectus. Curabitur ante dolor, ultricies nec mollis ut, elementum at ipsum. Suspendisse ac nisi ut est scelerisque semper. Donec sed felis pretium, fringilla nisl sit amet, vulputate eros. Vestibulum dolor justo, rhoncus vel posuere at, mattis quis velit. Duis efficitur eleifend lectus a tristique. Donec nec venenatis elit.</p>
						<i>Jan 500 - Dec 535</i>
						<a href="/" class="btn variant-filled">Detail</a>
					</div>
				</div>
				<hr class="col-span-4 mt-4 mb-4"/>
			</div>
		</div>
</div>
