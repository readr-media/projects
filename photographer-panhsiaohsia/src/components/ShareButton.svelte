<button class="share-button {$$props.class||''}">
  <img src="img/share.svg" alt="">
</button>

<style lang="scss">
  .share-button {
    width: 40px;
    height: 40px;
    background-color: white;
    border-radius: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      width: 70%;
      height: 70%;
    }
  }
</style>