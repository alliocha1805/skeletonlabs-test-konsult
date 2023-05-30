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
		'Nombre de consultant',
		'Nombre de mission',
    { 
        name: 'Liste consultant avec cette compétence',
        formatter: (cell, row) => {
          return h('button', {
            className: 'btn variant-filled-primary',
            onClick: () => routeToPage('competence/'+row.cells[0].data,false)
          }, 'Voir');
        }
      },
    { 
        name: 'Liste client demandant cette compétence',
        formatter: (cell, row) => {
          return h('button', {
            className: 'btn variant-filled-primary',
            onClick: () => routeToPage('competence/'+row.cells[0].data,false)
          }, 'Voir');
        }
      },
	]
  const data = [
    [ 1,"Management", 10, 2],
    [ 2,"Humour Noir", 2, 0],
		[ 3,"Beni des dieux", 1, 1],
    [ 4,"Depressif", 10, 0],
    [ 5,"Management", 10, 2],
		[ 6,"Management", 10, 2],
    [ 7,"Management", 10, 2],
    [ 8,"Management", 10, 2],
		[ 9,"Management", 10, 2],
		[ 10,"Management", 10, 2],
]

	const className = {
		table: 'table',
		paginationButton: 'btn variant-filled',
		paginationButtonCurrent: 'variant-filled-primary',
		input:'input',
		pagination: 'flex flex-col justify-end',
		header: "text-black",
		container : 'table-container',
    td: 'text-center',
    th: 'text-center'
	};
	const language = frFR;

</script>

<svelte:head>
	<title>Compétences</title>
	<meta name="description" content="Liste des clients" />
</svelte:head>

<div class="p-10 space-4">
  <h1 class="pb-5">Liste des Compétences</h1>
	<div id=my-grid-table>
		<Grid data={data} {columns} {className} language={language} search sort=true pagination={{ enabled: true, limit: 5}}/>
	</div>
</div>

<style>
td{
  text-align: 'center'
}
</style>