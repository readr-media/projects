{#if showHeader}
<header transition:fade="{{duration: 100}}" class="header">
  <div class="header__logo-share">
    <MirrorMediaLogo class="mirror-media-logo" />
    <ShareButton class="share-button" />
  </div>
</header>
{/if}

<svelte:window bind:scrollY={y}/>

<script>
  import MirrorMediaLogo from './MirrorMediaLogo.svelte'
  import ShareButton from './ShareButton.svelte'
  import { fade } from 'svelte/transition'

  let y = 0
  let oldY = 0

  let showHeader = true

  $: if (oldY !== y) {
    const isScrollingUp = y <= oldY
    showHeader = isScrollingUp
    oldY = y
  }
</script>

<style lang="scss">
.header {
  position: fixed;
  top: 10px;
  left: 0;
  width: 100%;
  &__logo-share {
    padding: 20px;
    display: inline-flex;
    align-items: center;
    & :global(.share-button) {
      margin: 0 0 0 10px;
    }
  }
}
</style>