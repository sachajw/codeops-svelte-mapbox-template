<script lang="ts">
  import { onMount } from 'svelte';
  import mapboxgl from 'mapbox-gl';

  // Add your Mapbox access token here
  mapboxgl.accessToken = 'ADD YOUR MAPBOX ACCESS TOKEN HERE';

  let mapContainer: HTMLDivElement;

  onMount(() => {
    const map = new mapboxgl.Map({
      container: mapContainer,
      style: 'mapbox://styles/mapbox/streets-v11',
      center: [20.0, 10.0], // Center of Africa
      zoom: 2.5
    });

    // Add navigation controls to the map
    map.addControl(new mapboxgl.NavigationControl());
  });
</script>

<style>
  #map {
    width: 1024px;
    height: 768px;
  }
</style>

<div id="map" bind:this={mapContainer}></div>