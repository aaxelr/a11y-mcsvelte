<script lang="ts">
  import { Meta, Template, Story } from '@storybook/addon-svelte-csf';
  import NumberInput from './NumberInput.svelte';
</script>

<Meta
  title="Input Components/Number Input"
  component={NumberInput}
  argTypes={{
    labelText: { defaultValue: 'Enter test number:', type: 'string', description: 'Label text' },
    labelTextColor: {
      defaultValue: 'black',
      type: 'string',
      description: 'Label text color',
    },
    value: { defaultValue: '', type: 'number', description: 'Number input field value' },
    fullWidth: { defaultValue: false, control: 'boolean', description: 'Full Width?' },
    step: { control: 'number', description: 'Step value' },
    minValue: { control: 'number', description: 'Minimum value' },
    maxValue: { control: 'number', description: 'Maximum value' },
  }}
/>

<Template let:args>
  <NumberInput {...args} />
</Template>

<Story name="Standard" args={{}} />

<Story
  name="Full-Width"
  args={{
    fullWidth: true,
  }}
/>
