<script lang="ts">
  export let title: string;
  export let description: string;
  export let url: string;
  export let image: string;
</script>

<svelte:head>
  <!-- Global Metadata -->
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width" />
  <link rel="shortcut icon" href="/favicon.ico" />

  <!-- Canonical URL -->
  <link rel="canonical" href={url} />

  <!-- Primary Meta Tags -->
  <title>{title}</title>
  <meta name="title" content={title} />
  <meta name="description" content={description} />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content={url} />
  <meta property="og:title" content={title} />
  <meta property="og:description" content={description} />
  {#if image}
    <meta property="og:image" content={image} />
  {/if}

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content={url} />
  <meta property="twitter:title" content={title} />
  <meta property="twitter:description" content={description} />
  {#if image}
    <meta property="twitter:image" content={image} />
  {/if}
</svelte:head>
