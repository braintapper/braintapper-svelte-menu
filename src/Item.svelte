<script>

  export let disabled = false;

  import { FlexRow, FlexRowCell } from "braintapper-svelte-flex";


  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;

</script>

<li menu-item {style} {id} class={classes}>
  <button type="button" on:click {disabled}>
    <div menu-label><slot></slot></div>       
  </button>
</li>


<style>
  li button {
    display: inline;
    border-radius: 0px;
    width: 100%;
    height: 100%;
    background: transparent;
    text-align: left;
    padding: 8px; }
    li button [menu-label], li button [menu-icon] {
      line-height: 24px; }
    li button [menu-label] {
      padding-top: 1px; }
    li button [menu-icon] {
      width: 32px;
      text-align: left; }




</style>