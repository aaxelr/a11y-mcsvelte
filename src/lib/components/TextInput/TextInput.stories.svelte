<script lang="ts">
  import { Meta, Template, Story } from '@storybook/addon-svelte-csf';
  import TextInput from './TextInput.svelte';
</script>

<Meta
  title="Input Components/Text Input"
  component={TextInput}
  argTypes={{
    labelText: { defaultValue: 'Enter test string:', type: 'string', description: 'Label text' },
    labelTextColor: {
      defaultValue: 'black',
      type: 'string',
      description: 'Label text color',
    },
    value: { defaultValue: '', type: 'string', description: 'Text input field value' },
    fullWidth: { defaultValue: false, control: 'boolean', description: 'Full width?' },
  }}
/>

<Template let:args>
  <TextInput {...args} />
</Template>

<Story name="Standard" />

<Story
  name="Full-Width"
  args={{
    fullWidth: true,
  }}
/>
