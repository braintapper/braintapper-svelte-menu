<script>

  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;

</script>

<ul role="menu" {style} {id} class={classes}>
  <slot/>
</ul>

<style>
  ul[role="menu"] {
    width: 100%;
    list-style-type: none;;
  }
</style>