<script>

  export let disabled = false;
  export let tabindex = undefined;

  import { FlexRow, FlexRowCell } from "braintapper-svelte-flex";


  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;

</script>

<li menu-item {style} {id} class={classes}>
  <button type="button" on:click {disabled} {tabindex}>
    <div menu-label><slot></slot></div>       
  </button>
</li>


<style>
  li button {
    margin-left: 0px !important;
    display: inline;
    border-radius: 0px;
    border: none;
    margin: 0px;
    width: 100%;
    height: 100%;
    background: transparent;
    text-align: left;
    padding: 8px; }
    li button [menu-label] {
      line-height: 24px; 
      padding-top: 1px; }
      
    li[menu-item] button:hover, li[menu-item] button:hover {
      background: var(--lightest-gray); }



</style>