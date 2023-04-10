<script>
import { Avatar } from '@skeletonlabs/skeleton';
import Chart from 'svelte-frappe-charts';
import { ProgressRadial } from '@skeletonlabs/skeleton';
import Timeline from '$lib/Timeline/Timeline.svelte';
 //utilisation de la librairie svelte de chart  https://github.com/himynameisdave/svelte-frappe-charts
 let data = {
    labels: ['Jan', 'Fev', 'Mar', 'Avr', 'Mai', 'Jui', 'Juil'],
    datasets: [
      {
        values: [8562, 8554, 10587, 6509, 620, 15000, 16000]
      }
    ]
  };
	let nbConsultant = 785	;
	let nbConsultantActif = 700	;
	let nbConsultantInterco = nbConsultant - nbConsultantActif;
	let pourcentageConsultantActif = nbConsultantActif/nbConsultant;
	let value = 85;
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Test Dashboard KOnsult.io avec Skeleton UI" />
</svelte:head>

<div class="p-10 space-4 grid-cols-1 gap-4 md:grid grid-cols-4 gap-2">
	<!--Card Graphique-->
	<div class="card p-4 col-span-4 2xl:col-span-2">
		<div class="p-4">
			<div class="">
				<p class="mb-0 font-sans font-semibold leading-normal text-lg">Chiffre d'affaire</p>
			<!--Il faut masquer en mobile le graph avec mediaqueries pour afficher juste les chiffres-->
				<div class=""><Chart data={data} type="line" /></div>
			</div>
		</div>
	</div>
	<!--Card avecc radial-->
	<div class="card p-4 col-span-2 2xl:col-span-1">
		<div class="p-4 flex flex-row -mx-3">
			<div class="flex-none w-2/3 max-w-full px-3">
				<p class="mb-0 font-sans font-semibold leading-normal text-lg">Consultants Actifs</p>
				<h5 class="text-green mb-0 font-bold">{nbConsultantActif}</h5>
			</div>
			<div class="px-3 text-right basis-1/3">
				<div class="inline-block w-12 h-12 text-center 500">
					<svg class="h-16 w-16 text-green-500"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/>
					</svg>
				</div>
			</div>
		</div>
		<div class="p-4 flex -mx-3 justify-center items-center grow h-3/5">
			<div class="">
				<ProgressRadial {value} stroke={100} meter="stroke-primary-500">{value}%</ProgressRadial>	
			</div>
		</div>
	</div>
	<!--Composant Timeline-->
	<Timeline />
	<div class="card p-4 col-span-2 2xl:col-span-1">
		<div class="p-4 flex flex-row -mx-3">
			<div class="flex-none w-2/3 max-w-full px-3">
				<p class="mb-0 font-sans font-semibold leading-normal text-lg">Clients Actifs</p>
				<h5 class="text-green mb-0 font-bold">85</h5>
			</div>
			<div class="px-3 text-right basis-1/3">
				<div class="inline-block w-12 h-12 text-center 500">
					<svg class="h-16 w-16 text-green-500"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/>
					</svg>
				</div>
			</div>
		</div>
	</div>
	<div class="card p-4 col-span-2 2xl:col-span-1">
		<div class="p-4 flex flex-row -mx-3">
			<div class="flex-none w-2/3 max-w-full px-3">
				<p class="mb-0 font-sans font-semibold leading-normal text-lg">Clients Inactifs</p>
				<h5 class="text-green mb-0 font-bold">24</h5>
			</div>
			<div class="px-3 text-right basis-1/3">
				<div class="inline-block w-12 h-12 text-center 500">
					<svg class="h-16 w-16 text-red-500"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 17h8m0 0V9m0 8l-8-8-4 4-6-6"/>
					</svg>
				</div>
			</div>
		</div>
	</div>
	<div class="table-container col-span-4">
		<table class="table-hover">
			<thead>
				<tr>
					<th>Position</th>
					<th>Name</th>
					<th>Symbol</th>
					<th>Weight</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td>1321</td>
					<td>1321</td>
					<td>1321</td>
					<td>1321</td>
				</tr>
			</tbody>
			<tfoot>
				<tr>
					<th colspan="3">Calculated Total Weight</th>
					<td>1587</td>
				</tr>
			</tfoot>		
		</table>
	</div>
</div>

<style>

</style>
