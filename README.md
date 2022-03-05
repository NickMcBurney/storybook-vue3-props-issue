# storybook-vue3-props-issue

### Case:
I have a component library which has a number of components using the same props, rather than duplicating the same prop setup across multiple components I used an external file to create props and import them into each component. The props are added to component props by adding via spread operator.

### Issue
Props defined at component level are shown in Storybook under the 'Props' heading. But the props imported to components are not shown here.
