<script>
	import { drawerStore } from '@skeletonlabs/skeleton';
  function drawerClose() 
  {
		drawerStore.close({});
	}
</script>

<nav class="list-nav p-4">
	<ul>
		<li><a href="/" on:click={drawerClose}>Homepage</a></li>
		<li><a href="/about" on:click={drawerClose}>About</a></li>
	</ul>
</nav>