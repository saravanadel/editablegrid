<script>
  export let value;
  export let editable = false;
</script>

<style>
 
</style>

<div>
  {#if !editable}
    <p on:mouseenter={e => (editable = true)}> {value} </p>
  {:else}
    <input on:focusout={e => (editable = false)} type="text" {value} />
  {/if}
</div>
