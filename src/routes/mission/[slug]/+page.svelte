<script lang="ts">
  import { page } from '$app/stores'
	import { Avatar } from '@skeletonlabs/skeleton';
</script>

<svelte:head>
	<title>Mission {$page.params.slug}</title>
	<meta name="description" content="Description mission {$page.params.slug}" />
</svelte:head>


<div class="p-10 grid grid-cols-4 gap-4">
  <div class="flex flex-col col-span-4 xl:col-span-1">
    <!--Bloc information-->
    <div class="card p-4 mb-4 bg-variant-filled-surface flex flex-col">
      <h3 class= "text-center xl:text-left">Informations</h3>
      <div class="flex flex-col">
        <div class="flex flex-row flex-wrap m-2" style="justify-content:space-between">
          <p>Contact:</p><a href="mailto:roi.arthur@kaamelott.fr">roi.arthur@kaamelott.fr</a>
        </div>
        <div class="flex flex-row m-2" style="justify-content:space-between">
          <p>Tel:</p><a href="tel:+33102030405">+33102030405</a>
        </div>
        <div class="flex flex-row m-2" style="justify-content:space-between">
          <p>TJM:</p><b>890</b>
        </div>
        <div class="flex flex-row m-2" style="justify-content:space-between">
          <p>Date début:</p><b>01/01/1970</b>
        </div>
        <div class="flex flex-row m-2" style="justify-content:space-between">
          <p>Date Fin:</p><b></b>
        </div>
        <div class="flex flex-row m-2" style="justify-content:space-between">
          <p>Status:</p><span class="chip variant-filled-primary m-1"><b>Actif</b></span>
        </div>
      </div>
    </div>
    <!--Bloc competences-->
    <div class="card p-4 bg-variant-filled-surface flex flex-col" style="justify-content:space-between;">
      <h3 class= "text-center xl:text-left">Skills</h3>
    </div>		
  </div>
  <div class="card p-4 col-span-4 bg-variant-filled-surface xl:col-span-3" style="justify-content:space-between;">
    <h3>Detail Mission</h3>
  </div>
</div>