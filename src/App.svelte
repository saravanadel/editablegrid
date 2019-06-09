<script>
  import EditableTable from "./EditableTable.svelte";
  let cols = ['Name','Age']
  let rows= [ ['Saravanan', '32'],  ['Saravanan', '32'] ]
  
</script>

<style>

</style>

<EditableTable cols={cols} rows={rows}  />
