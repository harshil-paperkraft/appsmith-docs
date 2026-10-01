---
Description: This page provides information on how to use the Calendar widget to show events in a month, week or day view and let users pick a date.
---
# Calendar

This page provides information on using the Calendar widget to show events in a month, week or day view and let users pick a date.

## Content properties

These properties are customizable options present in the property pane of the widget, allowing users to modify the widget according to their preferences.

### Data

#### Default Date `string`

<dd>

Sets the date shown when the page loads. The value is an ISO date string, such as `2026-03-12`.

You can display dynamic data by binding the response from a query or a JavaScript function to the **Default Date** property:

*Example*:

```js
{{DatePicker1.selectedDate}}
```

</dd>

### General

#### Show Weekends `boolean`

<dd>

Shows Saturday and Sunday in the calendar. The default value for the property is `true`.

</dd>

#### Visible `boolean`

<dd>

Controls the visibility of the widget. If you turn off this property, the widget would not be visible in View Mode. The default value for the property is `true`.

</dd>

### Events

When the event is triggered, these event handlers can execute queries, JS functions, or other [supported actions](/reference/appsmith-framework/widget-actions).

#### onDateSelected

<dd>

Specifies the action to be executed when a user picks a date.

</dd>

## Reference properties

Reference properties are properties that are not available in the property pane but can be accessed using the dot operator in other widgets or JavaScript functions. They provide additional information or allow interaction with the widget programmatically.

#### selectedDate `string`

<dd>

Contains the date the user picked.

*Example:*

```js
{{Calendar1.selectedDate}}
```

</dd>

## Methods

Widget property setters enable you to modify the values of widget properties at runtime, eliminating the need to manually update properties in the editor.

These methods are asynchronous and return a [Promise](/core-concepts/writing-code/javascript-promises#using-promises-in-appsmith). You can use the `.then()` block to ensure execution and sequencing of subsequent lines of code in Appsmith.

#### setVisibility (param: boolean): Promise

<dd>

Shows or hides the widget.

*Example*:

```js
Calendar1.setVisibility(true)
```

</dd>
