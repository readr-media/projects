<section class="app">
  {#if width <= 768}
    <Mobile class="mobile" />
  {:else}
    <Desktop class="desktop" />
  {/if}
</section>

<svelte:window bind:innerWidth={width}/>

<script>
  import Mobile from './views/Mobile.svelte'
  import Desktop from './views/Desktop.svelte'

  document.addEventListener('contextmenu', event => event.preventDefault())

  let width
</script>

<style lang="scss">
  //.app {
  //  :global(.mobile) {
  //    display: none;
  //  }
  //}
</style>