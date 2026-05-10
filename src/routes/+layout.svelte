<script lang="ts">
  import { asset } from '$app/paths';

	let { children } = $props();
</script>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    margin: 0;
    font-family: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    font-weight: 200;
    background: #000000;
    font-size: 16px;
  }
</style>

<svelte:head>
	<link rel="icon" href={asset("/y_production_logo_RGB.svg")} />
</svelte:head>

{@render children()}
