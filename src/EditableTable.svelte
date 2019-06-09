<script>
  import Cell from "./Cell.svelte";
  export let cols;
  export let rows;

  let editable = false;
</script>

<style>
  td {
    border-top: 1px solid grey;
    padding:0px;
    margin:0px;
  }
</style>

Editable
<input type="checkbox" bind:checked={editable} />
<table >
  <tr>
    {#each cols as heading}
      <th>{heading}</th>
    {/each}
  </tr>
  {#each rows as row}
    <tr>
      {#each row as val}
        <td>
          <Cell value={val} />
        </td>
      {/each}
    </tr>
  {/each}
</table>
