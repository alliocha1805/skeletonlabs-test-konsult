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
          <p>Client:</p><a href="/client/1">Kaamelott</a>
        </div>
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
    <div class="flex flex-row" style="justify-content:space-between">
      <h3 style="align-self:center">Detail Mission</h3>
      <a href="/" class="btn variant-filled-primary">
        <span><svg class="h-6 w-6 text-white"  viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <path d="M9 7 h-3a2 2 0 0 0 -2 2v9a2 2 0 0 0 2 2h9a2 2 0 0 0 2 -2v-3" />  <path d="M9 15h3l8.5 -8.5a1.5 1.5 0 0 0 -3 -3l-8.5 8.5v3" />  <line x1="16" y1="5" x2="19" y2="8" /></svg></span>
        <span>Editer</span>
      </a>    
    </div>

  </div>
</div>