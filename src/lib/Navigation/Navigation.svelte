<script>
	import { drawerStore } from '@skeletonlabs/skeleton';
  function drawerClose() 
  {
		drawerStore.close({});
	}
</script>

<nav class="list-nav p-4">
	<ul>
		<li><a href="/" on:click={drawerClose}><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <polyline points="5 12 3 12 12 3 21 12 19 12" />  <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />  <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" /></svg><b>_Homepage</b></a></li>
		<li><a href="/cra" on:click={drawerClose}><i>Compte Rendu d'Activité</i></a></li>
		<li><a href="/consultant" on:click={drawerClose}>Consultant</a></li>
		<li><a href="/mission" on:click={drawerClose}>Missions</a></li>
		<li><a href="/client" on:click={drawerClose}>Clients</a></li>
		<li><a href="/competence" on:click={drawerClose}>Compétences</a></li>
		<li><a href="/about" on:click={drawerClose}>About</a></li>
	</ul>
</nav>