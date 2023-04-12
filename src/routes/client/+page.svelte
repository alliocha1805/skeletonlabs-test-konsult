<script lang="ts">
  import Grid from "gridjs-svelte"
	import { frFR } from "gridjs/l10n";
	import { onMount, afterUpdate } from 'svelte';

  const data = [
    { name: "John", email: "john@example.com" },
    { name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
		{ name: "Mark", email: "mark@gmail.com" },
  ]

	const className = {
		table: 'table',
		paginationButton: 'btn variant-filled',
		paginationButtonCurrent: ' ml-2 mr-2',
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