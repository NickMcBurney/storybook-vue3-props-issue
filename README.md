# storybook-vue3-props-issue

### Case:
I have a component library which has a number of components using the same props, rather than duplicating the same prop setup across multiple components I used a [seperate file](https://github.com/NickMcBurney/storybook-vue3-props-issue/blob/main/src/stories/sharedProps.js) to create props and [import](https://github.com/NickMcBurney/storybook-vue3-props-issue/blob/0517df17be90f850aa3be438cf4396e7b0ff2f61/src/stories/Button.vue#L9) them into each component. The props are added to component props by adding via [spread operator](https://github.com/NickMcBurney/storybook-vue3-props-issue/blob/main/src/stories/Button.vue#L33).

### Issue
Props defined at component level are shown in Storybook under the 'Props' heading. But the props imported to components are not shown here.


### Screenshots:
Showing prop value (default value) working in Vue 3 template, but missing from Storybook 'Props' controls section

![image](https://user-images.githubusercontent.com/6604187/156893305-6cde828f-8943-48e2-9071-ca3551ad8273.png)

Showing prop value (set via Storybook args) - shown in controls but not 'Props' section

![image](https://user-images.githubusercontent.com/6604187/156893334-bc849a6b-01dd-41ef-9ab2-388f9a680230.png)

