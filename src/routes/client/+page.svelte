<script lang="ts">
  import Grid from "gridjs-svelte"
	import { frFR } from "gridjs/l10n";
	import { onMount, afterUpdate } from 'svelte';

  const data = [
    { name: "Kaamelott", secteur: "Militaire", actif : "Oui", consultants:12 },
    { name: "Royaume de l'Ogre", secteur: "Militaire", actif : "Oui", consultants:12 },
		{ name: "Francie", secteur: "Culture", actif : "Oui", consultants:12 },
		{ name: "Senat de Rome", secteur: "Toge", actif : "Oui", consultants:12 },
    { name: "Kaamelott", secteur: "Militaire", actif : "Oui", consultants:12 },
    { name: "Royaume de l'Ogre", secteur: "Militaire", actif : "Oui", consultants:12 },
		{ name: "Francie", secteur: "Culture", actif : "Oui", consultants:12 },
		{ name: "Senat de Rome", secteur: "Toge", actif : "Oui", consultants:12 },
    { name: "Kaamelott", secteur: "Militaire", actif : "Oui", consultants:12 },
    { name: "Royaume de l'Ogre", secteur: "Militaire", actif : "Oui", consultants:12 },
		{ name: "Francie", secteur: "Culture", actif : "Oui", consultants:12 },
		{ name: "Senat de Rome", secteur: "Toge", actif : "Oui", consultants:12 },
    { name: "Kaamelott", secteur: "Militaire", actif : "Oui", consultants:12 },
    { name: "Kaamelott", secteur: "Militaire", actif : "Oui", consultants:12 },
]

	const className = {
		table: 'table',
		paginationButton: 'btn variant-filled',
		paginationButtonCurrent: 'variant-filled-primary',
		input:'input',
		pagination: 'flex flex-col justify-end',
		header:"text-black"
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
		<Grid data={data} {className} language={language} search pagination={{ enabled: true, limit: 5}}/>
	</div>
</div>

<style>

</style>