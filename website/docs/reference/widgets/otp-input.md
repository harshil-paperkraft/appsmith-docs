# OTP Input

This page provides information on using the OTP Input widget, which allows you to capture one-time codes such as email verification codes, 2FA codes or PIN codes as input from users. The widget shows one box per character.

## Content properties

These properties are customizable options present in the property pane of the widget, allowing users to modify the widget according to their preferences.

### Data

#### Code length `number`

<dd>

Sets the number of boxes the widget displays. Each box holds one character.

*Constraints:* Minimum `4`, maximum `8`. Default `6`.

</dd>

#### Allowed characters `string`

<dd>

Sets the characters the widget accepts. Characters that aren't allowed are ignored when typed or pasted.

*Options:*
* **Numbers only**: Accepts digits only. Value `NUMERIC`.
* **Letters and numbers**: Accepts letters and digits. Value `ALPHANUMERIC`.

Default `NUMERIC`.

</dd>

#### Default value `string`

<dd>

Allows you to assign an initial value to the widget before user interaction. Characters that aren't allowed are dropped.

</dd>

### Label

#### Text `string`

<dd>

Sets the label on the widget, shown above the boxes. Default `Verification code`.

</dd>

### Validation

#### Required `boolean`

<dd>

When enabled, this property makes the OTP Input a mandatory field. Every box must be filled.

Default `false`.

</dd>

### General

#### Hide characters `boolean`

<dd>

When enabled, the widget shows dots instead of the characters.

Default `false`.

</dd>

#### Auto focus `boolean`

<dd>

When enabled, automatically places the user's cursor in the first box upon page load, directing their attention to the input field for immediate interaction.

Default `false`.

</dd>

#### Visible `boolean`

<dd>

Controls the visibility of the widget. If you turn off this property, the widget would not be visible in View Mode. Additionally, you can use JavaScript by clicking on **JS** next to the **Visible** property to conditionally control the widget's visibility.

Default `true`.

</dd>

#### Disabled `boolean`

<dd>

Prevents users from selecting the widget. Even though the widget remains visible, user input is not permitted. Additionally, you can use JavaScript by clicking on **JS** next to the **Disabled** property to control the widget's disable state conditionally.

Default `false`.

</dd>

#### Animate Loading `boolean`

<dd>

Controls whether the widget is displayed with a loading animation. When enabled, the widget shows a skeletal animation during the loading process. Additionally, you can control it through JavaScript by clicking on the **JS** next to the property.

Default `true`.

</dd>

### Events

When the event is triggered, these event handlers can run queries, JS code, or other [supported actions](/reference/appsmith-framework/widget-actions).

#### onChange

<dd>

Specifies the actions to be executed on every change to the code.

</dd>

#### onComplete

<dd>

Specifies the actions to be executed when the last empty box is filled.

</dd>
