  <header class="header">
    <div class="header__logo-share">
      <MirrorMediaLogo class="mirror-media-logo" />
      <ShareButton class="share-button" />
    </div>
  </header>

  <script>
    import MirrorMediaLogo from './components/MirrorMediaLogo.svelte'
    import ShareButton from './components/ShareButton.svelte'
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