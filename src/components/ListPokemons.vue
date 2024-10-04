<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"]);
</script>


<template>
  <div class="col-4 col-md-6 col-xl-3">
    <div class="card p-2 mb-3 cardListPokemon">
      <p class="text-center">{{ pokemon.name }}</p>
      <img :src="urlBaseSvg" class="card-img-top" alt="..." height="80" />
    </div>
  </div>
</template>

<style scoped>
.cardListPokemon {
  background: rgb(113, 129, 211);
  background: radial-gradient(
    circle,
    rgba(160, 163, 200, 0.749) 0%,
    rgba(81, 16, 211, 0.529) 100%
  );
}

.cardListPokemon:hover {
  background: rgb(113, 129, 211);
  background: radial-gradient(
    circle,
    rgba(160, 163, 200, 0.949) 0%,
    rgba(81, 16, 211, 0.729) 100%
  );
  cursor: pointer;
}

.cardListPokemon img:hover {
  padding: 0.1rem;
}
</style>