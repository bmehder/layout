<script>
  export let boxed = false;
  export let margin = "";
  export let padding = "";
  export let background = "";
  export let color = "";
</script>

<section
  class:boxed
  style="background:{background};color:{color};margin:{margin};padding:{padding};">
  <div class="content-wrap">
    <slot />
  </div>
</section>

<style>
  .boxed {
    max-width: 960px;
    margin: auto;
  }
  .content-wrap {
    max-width: 960px;
    margin: auto;
    padding: 2em;
  }
</style>
