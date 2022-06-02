<script lang="ts">
  // TODO: Break out common props
  export let labelText: string;
  export let labelTextColor: string = 'black';
  export let fullWidth: boolean;
  export let value: string;
</script>

<div>
  <label style='color: {labelTextColor}'>
    {labelText}
    <input type="text" bind:value class={fullWidth ? 'full-width' : ''} />
  </label>
</div>

<style>
  label {
    font-family: Helvetica, Arial, sans-serif;
    font-size: 1.2em;
  }
  .full-width {
    width: 100%;
  }
</style>
