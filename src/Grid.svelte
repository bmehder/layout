<script>
  export let columns = "1fr";
  export let gap = "";
  export let place = "";
</script>

<div
  class="grid-wrap"
  style="grid-template-columns:{columns};grid-gap:{gap};place-items:{place};">
  <slot />
</div>

<style>
  .grid-wrap {
    display: grid;
    max-width: 960px;
  }
  @media screen and (max-width: 480px) {
    .grid-wrap {
      display: block;
    }
  }
</style>
