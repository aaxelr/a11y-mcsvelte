<script lang="ts">
  export let labelText: string;
  export let labelTextColor: string = 'black';
  export let fullWidth: boolean;
  export let value: string;
  export let minValue: number;
  export let maxValue: number;
  export let step: number = 1;
</script>

<div>
  <label style='color: {labelTextColor}'>
    {labelText}
    <input
      type="number"
      bind:value
      {step}
      min={minValue}
      max={maxValue}
      class={fullWidth ? 'full-width' : ''}
    />
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
