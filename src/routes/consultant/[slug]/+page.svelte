<script lang="ts">
  import { page } from '$app/stores'
</script>

<svelte:head>
	<title>Consultant</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="p-10 space-4">
	<h1 class="pb-5">Page consultant : nom du consultant</h1>

	<p>
		Test pour rendre ca dynamique : id consultant ==> {$page.params.slug}
	</p>
	<pre>
  	{JSON.stringify($page, null, 2)}
	</pre>
</div>
