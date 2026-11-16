---
description: Learn how to use the Badge widget to display a short label in a colored pill.
---
# Badge

This page provides information on using the Badge widget, which displays a short label, such as a status or category, in a colored pill.

## Content properties

These properties are customizable options present in the property pane of the widget, allowing users to modify the widget according to their preferences.

### Data

#### Text `string`

<dd>

Sets the label to be displayed. Long text is cut off with an ellipsis.

</dd>

#### Status `string`

<dd>

Sets the color of the badge. Accepts one of the following values:

* `NEUTRAL`
* `INFO`
* `SUCCESS`
* `WARNING`
* `ERROR`

The default value is `INFO`. Invalid values fall back to `NEUTRAL`. You can use JavaScript to set the status dynamically.

*Example:*

```js
{{Table1.selectedRow.paid ? "SUCCESS" : "WARNING"}}
```

</dd>

### General

#### Tooltip `string`

<dd>

Sets the text shown when the user hovers over the badge. The default is empty.

</dd>

#### Visible `boolean`

<dd>

Controls the visibility of the widget. If you turn off this property, the widget is not visible in View Mode. The default is `true`.

</dd>

#### Animate Loading `boolean`

<dd>

This property controls whether the widget is displayed with a loading animation. The default is `true`.

</dd>

### Events

#### onClick `action`

<dd>

Sets an action to run when the badge is clicked. The badge is only clickable, with a pointer cursor and keyboard focus, when this property is set.

</dd>

## Style properties

Style properties allow you to change the look and feel of the widget.

### General

#### Variant `string`

<dd>

Sets the visual style of the badge. Accepts one of the following values:

* `SOLID`
* `SUBTLE`
* `OUTLINE`

The default is `SUBTLE`.

</dd>

### Border and shadow

#### Border radius `string`

<dd>

Applies rounded corners to the outer edge of the widget. The default is the theme border radius.

</dd>

## Reference properties

Reference properties are properties that are not available in the property pane but can be accessed using the dot operator in other widgets or JavaScript functions. For instance, to get the text of a Badge widget, you can use `Badge1.text`.

#### text `string`

<dd>

The `text` property retrieves the current label of the widget.

*Example:*

```js
{{Badge1.text}}
```

</dd>

#### status `string`

<dd>

The `status` property retrieves the current status of the widget.

*Example:*

```js
{{Badge1.status}}
```

</dd>

#### isVisible `boolean`

<dd>

The `isVisible` property indicates the visibility state of the widget, with `true` indicating it is visible and `false` indicating it is hidden.

*Example:*

```js
{{Badge1.isVisible}}
```

</dd>

## Methods

Widget property setters enable you to modify the values of widget properties at runtime, eliminating the need to manually update properties in the editor.

These methods are asynchronous, and you can use the `.then()` block to ensure execution and sequencing of subsequent lines of code in Appsmith.

#### setText (param: string): Promise

<dd>

Sets the text of the widget.

*Example:*

```js
Badge1.setText("New")
```

</dd>

#### setStatus (param: string): Promise

<dd>

Sets the status of the widget.

*Example:*

```js
Badge1.setStatus("SUCCESS")
```

</dd>

#### setVisibility (param: boolean): Promise

<dd>

Sets the visibility of the widget.

*Example:*

```js
Badge1.setVisibility(true)
```

</dd>
