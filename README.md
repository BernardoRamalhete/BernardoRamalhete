# Docs

# Components

### Use multi-worded component names

Component names should always be multi-word to prevent conflicts with existing and future HTML elements

```jsx
//Don't
export  default {
    name: 'Todo',
    // ...
}

//Do
 export  default {
    name: 'TodoItem',
    // ...
}
```

### All components and page files must be in PascalCase

This is the best casing for IDE's autocompletion and maintains a consistence between components in JS(X) and templates

```jsx
//Don't
components/
|-mycomponent.vue
|-myOtherComponent.vue

//Do
|-MyComponent.vue
|-MyOtherComponent.vue
```

### Components that are to be used on the whole project, base components, or components from the design system must have the specific 'App' prefix

```jsx
//Don't
components/
|-MyButton.vue
|-Icon.vue

//Do
components/
|-AppButton.vue
|-AppIcon.vue
```

### Components that are to be used only once *per page* must have the 'The' prefix

Components that are to be used only once <i>per page</i> must have the 'The' prefix

```markdown
//Don't
components/
|-Heading.vue
|-Sidebar.vue
|-Footer.vue
 
 //Do
 components/
 |-TheHeading.vue
 |-TheSidebar.vue
 |-TheFooter.vue
```

### Components that are related should include it's parent component as a prefix

This makes the relationship between components evident and makes sure related files are next to each other on the IDE's file explorer

```jsx
//Don't
components/
|- TodoList.vue
|- TodoItem.vue
|- TodoButton.vue

//Do
|- TodoList.vue
|- TodoListItem.vue
|- TodoListItemButton.vue
```

### Component names should start with the most general word and end with the most descriptive one

This standart makes it easier to find related components and to identify then by it's function

```jsx
//Don't
components/
|- ClearSearchButton.vue
|- ExcludeFromSearchInput.vue
|- LaunchOnStartupCheckbox.vue
|- RunSearchButton.vue
|- SearchInput.vue
|- TermsCheckbox.vue

//Do
components/
|- SearchButtonClear.vue
|- SearchButtonRun.vue
|- SearchInputQuery.vue
|- SearchInputExcludeGlob.vue
|- SettingsCheckboxTerms.vue
|- SettingsCheckboxLaunchOnStartup.vue
```
