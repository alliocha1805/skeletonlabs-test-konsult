<script lang="ts">
  import Grid from "gridjs-svelte"
	import { frFR } from "gridjs/l10n";
	import { onMount, afterUpdate } from 'svelte';
	import { h, PluginPosition } from "gridjs";	
	import { goto } from '$app/navigation';
	function routeToPage(route: string, replaceState: boolean) {
   goto(`/${route}`, { replaceState }) 
	}

	const columns=[
		{
			name:'id',
			hidden:true},
		'client',
		'type mission',
		'date debut',
		'date fin',
		'TJM',
		{
			name: 'Action',
			formatter: (cell, row) => {
				return h('button', {
					onClick: () => {
						routeToPage('mission/'+row.cells[0].data,false);
					}
				}, 'Voir la page mission');
			}
		}
	]
  const data = [
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 2,"Du Lac","Lancelot", "Traître", "Oui", "Meleagant", null],
		[ 3,"Meleagant","???", "Incarnanation du mal ?", "Oui", "???", null],
		[ 4,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
		[ 1,"Pendragon","Arthur", "Roi de Bretagne", "Oui", "Dieu", null],
]

	const className = {
		table: 'table',
		paginationButton: 'btn variant-filled',
		paginationButtonCurrent: 'variant-filled-primary',
		input:'input',
		pagination: 'flex flex-col justify-end',
		header: "text-black",
		container : 'table-container'
	};
	const language = frFR;

</script>

<svelte:head>
	<title>Liste des Missions</title>
	<meta name="description" content="Liste des consultants" />
</svelte:head>

<div class="p-10 space-4">
  <h1 class="pb-5">Liste des Missions</h1>
	<div id=my-grid-table>
		<Grid data={data} {columns} {className} language={language} search pagination={{ enabled: true, limit: 10}}/>
	</div>
</div>
