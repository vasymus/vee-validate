---
title: Checkbox and Radio Inputs
description: Validating checkboxes and Radio inputs
order: 1
---

# Checkbox and Radio Inputs

The documentation has so far avoided using `type="radio"` and `type="checkbox"` inputs because of their complex nature, however vee-validate supports both HTML checkboxes and radio inputs as well as your custom components that act as such (with caveats).

The only requirements are that the fields:

<div class="features">

- Must be inside a `Form` component or a [derivative (using useForm)](/api/use-form#creating-custom-form-components)
- Must Have the same `name` prop
- Should have a `type` attribute

</div>

<doc-tip title="Slot props and custom components">

When using `Field` slot props with checkbox/radio components, you still need to provide the `type` and `value` props to the `Field` node itself.

```vue
<Field v-slot="{ field }" name="terms" type="checkbox" :value="false">
  <label>
    <input type="checkbox" name="terms" v-bind="field" :value="false" />
    I agree
  </label>
</Field>
```

The same caveat applies if you are rendering another component with `as` prop:

```vue
<Field as="my-checkbox" name="terms" type="checkbox" :value="false" />
```

</doc-tip>

## Validating Radio Inputs

vee-validate handles radio input groups as long as they have the `type="radio"` and the same `name` prop value. The selected value will be present in the `values` object.

<live-example id="vee-validate-v4-radio"></live-example>

## Validating Checkbox Inputs

vee-validate handles checkboxes as long as they have the `type="checkbox"` prop and the same `name` prop value. The selected values will be collected in an array similar to what `v-model` does.

<live-example id="vee-validate-v4-checkboxes"></live-example>

If there is only one checkbox then its value will be directly assigned in the `values` object without binding it in an array.
