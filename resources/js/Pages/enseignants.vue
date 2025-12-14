<script setup>
defineProps({
enseignants: Array
})
</script>


<template>
<div class="p-6">
<h1 class="text-2xl font-bold mb-4">Liste des Enseignants</h1>


<table class="w-full border">
<thead class="bg-gray-100">
<tr>
<th>Matricule</th>
<th>Nom</th>
<th>Spécialité</th>
<th>Étudiants Encadrés</th>
</tr>
</thead>
<tbody>
<tr v-for="ens in enseignants" :key="ens.id" class="border-t">
<td>{{ ens.matricule }}</td>
<td>{{ ens.nom }} {{ ens.prenom }}</td>
<td>{{ ens.specialite }}</td>
<td>
<ul>
<li v-for="et in ens.etudiants" :key="et.id">
{{ et.nom }} {{ et.prenom }}
</li>
</ul>
</td>
</tr>
</tbody>
</table>
</div>
</template>