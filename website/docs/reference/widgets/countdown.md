---
description: Learn how to use the Countdown widget to show the time left until a target date and run an action when it reaches zero.
---
# Countdown

This page provides information on using the Countdown widget, which shows the time left until a target date and runs an action when it reaches zero.

## Content properties

These properties are customizable options present in the property pane of the widget, allowing users to modify the widget according to their preferences.

### Data

#### Target date `string`

<dd>

Sets the date and time the countdown counts down to, as an ISO date string. You can also use values retrieved from queries or JavaScript functions within the mustache operator `{{}}`.

</dd>

#### Format `string`

<dd>

Sets the units the countdown displays.

*Options:*
* `DD:HH:MM:SS`
* `HH:MM:SS`
* `MM:SS`

Units that are not shown roll into the largest unit that is shown, so 2 hours in `MM:SS` reads `120:00`.

</dd>

#### Completed text `string`

<dd>

Sets the text shown in place of the timer when the countdown reaches zero.

</dd>

### General

#### Visible `boolean`

<dd>

Controls the visibility of the widget. If you turn off this property, the widget would not be visible in View Mode. Additionally, you can use JavaScript by clicking on **JS** next to the **Visible** property to conditionally control the widget's visibility.

</dd>

#### Animate Loading `boolean`

<dd>

This property controls whether the widget is displayed with a loading animation. When enabled, the widget shows a skeletal animation during the loading process. Additionally, you can control it through JavaScript by clicking on the <code>JS</code> next to the property.

</dd>

### Events

#### onComplete

This event defines the action that would be executed once when the countdown reaches zero. It allows you to specify a list of [supported actions](/reference/appsmith-framework/widget-actions) that can be triggered in response to the countdown completing.

## Style properties
Style properties allow you to change the look and feel of the widget.

#### Font color `string`

<dd>

Represents the text color of the widget, specified as a [CSS color value](https://developer.mozilla.org/en-US/docs/Web/CSS/color). It can also be manipulated programmatically using the JavaScript functions.

</dd>

#### Font size `string`

<dd>

Determines the font size of the countdown. It accepts [CSS font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size) values and can also be programmatically modified using JavaScript functions.

</dd>

## Reference properties

These properties are not available in the property pane, but can be accessed using the dot operator in other widgets or JavaScript functions. For instance, to get the visibility status, you can use `Countdown1.isVisible`.

#### isComplete `boolean`
<dd>

The `isComplete` property indicates whether the countdown has reached zero. It is represented by a boolean value, where true signifies that the countdown is complete, and false signifies that it is still running. Changing the target date sets `isComplete` back to `false`.

</dd>

#### targetDate `string`
<dd>

The `targetDate` property reflects the date and time the countdown counts down to.

</dd>

#### isVisible `boolean`
<dd>

The `isVisible` property reflects the state of the widget's **Visible** setting. It is represented by a boolean value, where true indicates that the widget is visible, and false indicates that it is hidden or not displayed on the page.
</dd>

## Methods

Widget property setters enable you to modify the values of widget properties at runtime, eliminating the need to manually update properties in the editor.

These methods are asynchronous and return a [Promise](/core-concepts/writing-code/javascript-promises#using-promises-in-appsmith). You can use the `.then()` block to ensure execution and sequencing of subsequent lines of code in Appsmith.

#### setTargetDate (param: string): Promise

<dd>

Sets the target date of the Countdown widget.

*Example*:

```js
Countdown1.setTargetDate("2026-03-12T00:00:00.000Z")
```

</dd>

#### setVisibility (param: boolean): Promise

<dd>

Sets the visibility of the widget.

*Example*:

```js
Countdown1.setVisibility(true)
```

</dd>
