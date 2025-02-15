---
title: Custom Inputs
description: Building custom inputs with useField()
order: 2
---

# Custom Inputs

More often than not, you will have complex requirements for your inputs. Like a custom design, multiple UI states, validation and more. You can easily build your custom components with `useField()` composable function. While it is possible to build your inputs with `<Field />` component it is not recommended as you won't have access to many of the underlying features to manage your UI state and you would rely on scoped slot props which is only available in the template.

`useField` allows you to hook into the many underlying features of the `Field` component in a composable manner that you can easily integrate it in your UI, and on top of that your custom components will work seamlessly with `<Form />` component or `useForm` without any intervention on your part.

In the following example we have a complex `TextInput` component that we use for many types of fields.

<live-example id="vee-validate-v4-custom-inputs"></live-example>
