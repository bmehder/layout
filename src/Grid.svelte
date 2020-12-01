<script>
  export let columns = "1fr";
</script>

<div class="grid-wrap" style="grid-template-columns:{columns};">
  <slot />
</div>

<style>
  .grid-wrap {
    display: grid;
    grid-gap: 2em;
    place-items: center;
    max-width: 960px;
  }
  @media screen and (max-width: 480px) {
    .grid-wrap {
      display: block;
    }
  }
</style>
