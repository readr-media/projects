<figure class="figure">
  <Lazy
    height={height}
    offset={0}
  >
    <img
      src="img/{figureName}.jpg"
      alt="{figureName}"
    >
  </Lazy>
  <figcaption>{figcaption}</figcaption>
</figure>

<svelte:window
  bind:innerWidth={windowInnerWidth}
/>

<script>
  import Lazy from './Lazy.svelte'

  export let figureName
  export let figcaption
  export let imgIntrinsicsize = [0, 0]
  let windowInnerWidth = 0
  $: height = (imgIntrinsicsize[1] / imgIntrinsicsize[0]) * (windowInnerWidth - 40)
</script>

<style lang="scss">
  .figure {
    width: 100%;
    margin: 20px 0 0 0 ;
    position: relative;
    z-index: -1;
    img {
      width: 100%;
    }
    figcaption {
      margin: 10px 0 0 0;
      font-size: 14px;
      line-height: 2;
    }
  }
</style>