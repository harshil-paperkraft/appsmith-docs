---
description: >-
  Segmented Control widget reference
---

# Segmented Control

This page provides information on the Segmented Control widget, which shows 2 to 5 options as a row of joined buttons and lets the user pick one.

Use it for short lists where every option should stay visible, such as Day, Week or Month. A Select widget hides the same options in a dropdown.

## Content properties

These properties are customizable options present in the property pane of the widget, allowing users to modify the widget according to their preferences.

### Data

#### Options `array of objects`

Specify the options as an array of objects, each with a `label` and a `value`. The widget accepts 2 to 5 options. Every option needs a label, and the values must be unique. The default options are Day, Week and Month.

You can turn on **JS** and provide the options as JavaScript, for example to build them from a query response.

#### Default selected value `string`

Sets the option that is selected when the widget loads. The default is `WEEK`. Leave the property empty to start with nothing selected. A value that matches no option also selects nothing.

### Label

#### Text `string`

Sets the label of the widget, shown above the segments. The default is empty.

### General

#### Fill width `boolean`

Controls whether the segments stretch to fill the width of the widget. The default is `true`. When turned off, each segment is only as wide as its label.

#### Visible `boolean`

Controls the visibility of the widget. If you turn off this property, the widget is not visible in View mode. Additionally, you can use JavaScript by clicking on **JS** next to the **Visible** property to control the widget's visibility conditionally.

#### Disabled `boolean`

Prevents users from selecting the widget. Even though the widget remains visible, user input is not permitted. Additionally, you can use JavaScript by clicking on **JS** next to the **Disabled** property to control the widget's disabled state conditionally.

#### Animate Loading `boolean`

Controls whether the widget is displayed with a loading animation. When enabled, the widget shows a skeletal animation during the loading process. Additionally, you can control it through JavaScript by clicking on the **JS** next to the property.

### Events

#### onSelectionChange

Allows you to configure one or multiple actions (Framework functions, queries, or JS functions) to be executed when the user picks a different segment. Clicking the selected segment again does nothing.

## Style properties

Style properties allow you to change the look and feel of the widget.

#### Accent color `string`

Sets the background of the selected segment. The default is the theme primary color.

#### Border radius `string`

Applies rounded corners to the widget.
