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
		'nom',
		'secteur',
		'actif',
		'consultants',
    { 
        name: 'Actions',
        formatter: (cell, row) => {
          return h('button', {
            className: 'btn variant-filled-primary',
            onClick: () => routeToPage('client/'+row.cells[0].data,false)
          }, 'Voir');
        }
      },
	]
  const data = [
    [ 1,"Kaamelott", "Militaire", "Oui", 12, null],
    [ 2,"Royaume de l'Ogre", "Militaire", "Oui", 12, null],
		[ 3, "Francie", "Culture", "Oui", 12, null],
		[ 4,"Senat de Rome", "Toge", "Oui", 12, null],
    [ 5,"Kaamelott", "Militaire", "Oui", 12, null],
    [ 6,"Royaume de l'Ogre", "Militaire", "Oui", 12, null],
		[ 7,"Francie", "Culture", "Oui", 12, null],
		[ 8,"Senat de Rome", "Toge", "Oui", 12, null],
    [ 9,"Kaamelott", "Militaire", "Oui", 12, null],
    [ 10,"Royaume de l'Ogre", "Militaire", "Oui", 12, null],
		[ 11,"Francie", "Culture", "Oui", 12, null],
		[ 12,"Senat de Rome", "Toge", "Non", 12, null],
    [ 13,"Kaamelott", "Militaire", "Oui", 12, null],
    [ 14,"Kaamelott", "Militaire", "Oui", 12, null],
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
	<title>Clients</title>
	<meta name="description" content="Liste des clients" />
</svelte:head>

<div class="p-10 space-4">
  <h1 class="pb-5">Liste des Clients</h1>
	<div id=my-grid-table>
		<Grid data={data} {columns} {className} language={language} search sort=true pagination={{ enabled: true, limit: 5}}/>
	</div>
</div>

<style>

</style>