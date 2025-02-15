---
title: State Stores
description: using vee-validate with state stores
order: 8
new: true
---

# Stores

If you want to integrate vee-validate with state management solutions you can do that with the composition API.

## Pinia

[Pinia](https://pinia.esm.dev/) is a data store for Vue.js and it is the recommended solution to your Vue.js state management.

The example integrates a form state into the store by utilizing a setup function when defining a store. This makes vee-validate act as a state provider for the form where the form values become your store state and submit function becomes your store action.

<doc-tip>

Notice the errors are displayed immediately, this is because when using `useFieldModel` vee-validate can no longer detect the field touched state. If you want to control the validation behavior in this case, then you need to implement a custom component with `useField` or `<Field>`.

</doc-tip>

<live-example id="vee-validate-v4-pinia"></live-example>
