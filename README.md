# content-projection

In Angular, content projection is a powerful feature that allows you to pass content from a parent component to its child component,
giving you more flexibility in component composition and reusability.

Content projection is particularly useful when you want to create reusable components that can accept different content without sacrificing
their functionality or layout. It enables you to define a placeholder within a component's template where the content can be injected from the parent component.

To implement content projection in Angular, you need to use the <ng-content> element in the child component's template. The <ng-content> element
acts as a placeholder for the content that will be projected into it.

Here's a simple example to illustrate content projection:
  
```typescript
"<!-- parent.component.html -->"
"<div>"
  "<h2>Welcome to the parent component!</h2>"
  "<app-child>"
    "<h3>This is the projected content</h3>"
    "<p>Some additional text</p>"
  "</app-child>"
"</div>"

<!-- child.component.html -->
<div>
  <h4>This is the child component</h4>
  <ng-content></ng-content>
</div>
```

In the above example, we have a parent component that includes an app-child component. Inside the app-child component tags, we have included
some content, including an h3 and p element. This content will be projected into the <ng-content> placeholder in the child component's template.

When the parent component is rendered, the content provided within the app-child tags will be injected into the ng-content element in the child
component's template. The child component's template acts as a wrapper for the projected content, allowing you to combine the parent and child component's
content in a flexible manner.

The resulting output will be:

Welcome to the parent component!

This is the child component
This is the projected content
Some additional text
  
As you can see, the content provided in the parent component is projected into the child component, allowing you to combine both the parent and
child component's content seamlessly.

Content projection in Angular is a powerful feature that enables you to create more versatile and reusable components by allowing dynamic content
injection from the parent component. It provides a way to decouple the structure and layout of components from their content, leading to more flexible
and modular code.
