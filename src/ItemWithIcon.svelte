<script>

  export let disabled = false;

  import { FlexRow, FlexRowCell } from "braintapper-svelte-flex"

</script>

<li menu-item>
  <button type="button" on:click {disabled}>
    <FlexRow style="line-height: 24px">
      <FlexRowCell flex="initial">
        <div menu-icon><slot name="icon"/></div>
      </FlexRowCell>
      <FlexRowCell flex><div menu-label><slot></slot></div></FlexRowCell>
    </FlexRow>            
  </button>
</li>


<style>


  li[menu-item] button {
    margin-left: 0px !important;
    display: inline;

    border-radius: 0px;
    width: 100%;
    height: 100%;
    background: transparent;
    text-align: left;
    padding: 8px; }

    li[menu-item] button [menu-label], li[menu-item] button [menu-icon] {
      line-height: 24px; }

    li[menu-item] button [menu-label] {
      padding-top: 1px; }

    li[menu-item] button [menu-icon] {
      width: 32px;
      text-align: left; }

    li[menu-item] button[indent] {
      border-radius: 4px;
      width: auto;
      font-weight: bold; }

      li[menu-item] button[indent]:first-of-type {
        margin-left: 2px; }

    li[menu-item] button:hover {
      background: var(--lightest-gray); }

      /* global? */
      li[menu-item] button:hover svg path {
        fill: var(--blue) !important; }
    /* global? */
    li[menu-item] button svg path {
      fill: var(--black) !important; }

    li[menu-item] button[disabled] {
      color: var(--light-gray); }

      /* global? */
      li[menu-item] button[disabled] svg path {
        fill: var(--light-gray) !important; }


</style>