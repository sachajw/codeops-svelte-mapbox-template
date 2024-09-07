<script lang="ts">
  import AfricaMap from './components/AfricaMap.svelte';
</script>

<main>
  <h1>African Continent</h1>
  <AfricaMap />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    margin: 0;
  }

  h1 {
    margin-bottom: 20px;
  }
</style>