<svelte:head>
	<title>Clients</title>
	<meta name="description" content="Liste des clients" />
</svelte:head>

<div class="p-10 space-4">
  <h1 class="pb-5">Liste des Clients</h1>
  <div class="table-container text-token col-span-4 bg-surface-800">
      <table class="table-hover table-comfortable w-full">
        <thead class="h-14 bg-surface-700">
          <tr class="mb-5">
            <th colspan="5">
              <div class="flex flex-row p-4 justify-end">
                <input type='search' class="input mr-5 md:w-2/5 mr-10 variant-filled" placeholder="Rechercher un client par nom"/>
                <div class="flex flex-col justify-center">
                  <svg class="h-8 w-8 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="10" cy="10" r="7" />  <line x1="21" y1="21" x2="15" y2="15" /></svg>
                </div>
              </div>
            </th>
          </tr>
          <tr>
            <th class="table-cell-fit">Nom</th>
            <th class="table-cell-fit">Secteur</th>
            <th class="table-cell-fit">Actif ?</th>
            <th class="table-cell-fit">CA généré mois passé</th>
            <th class="table-cell-fit">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="table-cell-fit text-center">Chateau de Kaamelott</td>
            <td class="table-cell-fit text-center">Militaire</td>
            <td class="table-cell-fit text-center">Oui</td>
            <td class="table-cell-fit text-center">9840</td>
            <td class="table-cell-fit text-center">
            <span class="chip variant-soft hover:variant-filled">
              <span><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="12" cy="12" r="1" />  <circle cx="12" cy="19" r="1" />  <circle cx="12" cy="5" r="1" /></svg></span>
            </span>
            </td>
          </tr>
          <tr>
            <td class="table-cell-fit text-center">Chateau de Kaamelott</td>
            <td class="table-cell-fit text-center">Militaire</td>
            <td class="table-cell-fit text-center">Oui</td>
            <td class="table-cell-fit text-center">9840</td>
            <td class="table-cell-fit text-center">
            <span class="chip variant-soft hover:variant-filled">
              <span><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="12" cy="12" r="1" />  <circle cx="12" cy="19" r="1" />  <circle cx="12" cy="5" r="1" /></svg></span>
            </span>
            </td>
          </tr>
          <tr>
            <td class="table-cell-fit text-center">Chateau de Kaamelott</td>
            <td class="table-cell-fit text-center">Militaire</td>
            <td class="table-cell-fit text-center">Oui</td>
            <td class="table-cell-fit text-center">9840</td>
            <td class="table-cell-fit text-center">
            <span class="chip variant-soft hover:variant-filled">
              <span><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="12" cy="12" r="1" />  <circle cx="12" cy="19" r="1" />  <circle cx="12" cy="5" r="1" /></svg></span>
            </span>
            </td>
          </tr>
          <tr>
            <td class="table-cell-fit text-center">Chateau de Kaamelott</td>
            <td class="table-cell-fit text-center">Militaire</td>
            <td class="table-cell-fit text-center">Oui</td>
            <td class="table-cell-fit text-center">9840</td>
            <td class="table-cell-fit text-center">
            <span class="chip variant-soft hover:variant-filled">
              <span><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="12" cy="12" r="1" />  <circle cx="12" cy="19" r="1" />  <circle cx="12" cy="5" r="1" /></svg></span>
            </span>
            </td>
          </tr>
          <tr>
            <td class="table-cell-fit text-center">Chateau de Kaamelott</td>
            <td class="table-cell-fit text-center">Militaire</td>
            <td class="table-cell-fit text-center">Oui</td>
            <td class="table-cell-fit text-center">9840</td>
            <td class="table-cell-fit text-center">
            <span class="chip variant-soft hover:variant-filled">
              <span><svg class="h-4 w-4 text-white"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <circle cx="12" cy="12" r="1" />  <circle cx="12" cy="19" r="1" />  <circle cx="12" cy="5" r="1" /></svg></span>
            </span>
            </td>
          </tr>
        </tbody>
        <tfoot class="p-4">
          <tr>
            <th colspan="5" class="p-5"><a href="/consultant" class="btn variant-filled">Voir tous les clients</a></th>
          </tr>
        </tfoot>		
      </table>
    </div>
</div>