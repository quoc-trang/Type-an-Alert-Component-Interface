---
difficulty: 1
training: true
chapter: "Chapter 6: TypeScript"
tags: vue
---

# Type Provide/Inject Challenge

In this challenge, let's update the `vTabs` component created earlier on in the training to be type safe.

Use TypeScript to type the data injected via `vTabs` for use within `vTabPanel`.

## Requirements

1. On line 26 of `vTabs.vue` properly type the injectionKey as an `InjectionKey` that provides an object with the following properties:
   1. `registerTab` - a function that takes a title argument that's a string and returns void
   2. `activeTab` - a readonly reactive ref that is a a string or undefined
   3. `activateTab` - a function that takes a title argument that's a string and returns void
2. Once the types are in place, all TS errors in `vTabPanel.vue` should disappear

## TS errors exist in `vTabPanel.vue` before Provided Data is Typed

![Screenshot of the solution](https://images.certificates.dev/csvd-training-code-challenge-before-22.png)

## At the End, Those Errors Should Disappear

![Screenshot of the solution](https://images.certificates.dev/csvd-training-code-challenge-22.png)
