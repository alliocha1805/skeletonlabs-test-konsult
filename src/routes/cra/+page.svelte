<script lang="ts">
	import Tabulator from '$lib/Tabulator/Tabulator.svelte';
	let donnees={};
	let colonne={};
</script>

<svelte:head>
	<title>Comptes Rendus D'activité</title>
	<meta name="description" content="Comptes rendus d'activité" />
	<link href="https://unpkg.com/tabulator-tables@4.9.1/dist/css/tabulator.min.css" rel="stylesheet">
</svelte:head>

<!--Une idée serait d'avoir deux "picker" : MOIS et ANNEE ou un Range picker de date. A partir de la on affichera une Grid custom avec le plugin https://revolist.github.io/revogrid/. Ce plugin peut stocker en fichier/blob ou string-->
<div class="p-10 grid grid-cols-4 gap-4">
	<div class="flex flex-col col-span-4 xl:col-span-1">
		<div class="card p-4 bg-variant-filled-surface flex flex-col">
			<h3>Mon équipe</h3>
		</div>
	</div>
	<div class="card p-4 mb-4 bg-variant-filled-surface flex flex-col col-span-4 xl:col-span-3">
		<h3>Feuille de temps</h3>
		<Tabulator data={donnees} autoColumns=true/>
	</div>
</div>
