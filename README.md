# About ReactSymbols

## Setup




### Demo app

### Use in your project

Be sure that **you have installed all required NPM packages** you need for smooth setup of ReactSymbols UI Kit. Install all of them by one simple line:
```
npm install prop-types react-icons classnames react-select --save
```

1) Move `ReactSymbolsKit.js` and `ReactSymbolsKit.css` into your `src` folder
2) Link Component you want to use and files you moved into the project before:
```javascript
import './ReactSymbolsKit.css'
import { RSInput, RSButton } from './ReactSymbolsKit.js'
```
2) Link Component you want to use and files you moved into the project before:
```javascript
import './ReactSymbolsKit.css'
import { RSInput, RSButton } from './ReactSymbolsKit.js'
```
3) Define component you want to use. For example:
```javascript
<RSButton
	value='Your first RSButton'
	onClick={this.onClick.bind(this)}
/>
```


#### Files naming
Naming of all Components and their SASS files starts with `RS` for example `RSButton.js` or `RSButton.scss`. We don't want to create mess into your app or fight names of your existing files. It's also good for identification of code from ReactSymbols UI Kit.

#### UI Kit Preview
Imediatelly after setup you can see all components live on Example page. It's mix of variant's of each component. Basic action handelings are there coded as well, so you can use it how you want and you can see how to pass all the props and functions correctly.

# Project Setup

Let's see how easy and fast is setup process of ReactSymbols UI Kit.

## Building ReactJS app from scratch

## Into existing projects



### How to build SASS files to be able change color schema of most of component by one color definition

If you want to customize colors of your styles based on your brand colors, you can do it easily by modifying sass variables at **./styles/sass/RSDefaults.sass**. Just go there and modify variables as you need.

Once you are finished with that, you have to compile sass files into css again. Probably the easiest way is to use npm module *node-sass-chokidar*.
If you don't have this module in your project, just type following command in root of your project:

`npm install node-sass-chokidar`

This command will install module and all its dependencies. After that just build sass with following command (from root of your project ofc):

`./node_modules/.bin/node-sass-chokidar ./<path to react symbols folder>/styles/sass/ -o ./<path to react symbols folder again>/styles/css/`

And lastly refresh your project and you should see React Symbols Kit in theme of your brand colors.

<br>
### How variables in CONSTANTS works and what you can setup there

<br>

-----

# EVERYTHING BELOW SHOULD BE FINAL
👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼👇🏼

-----

# **Components**

## Alert

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**visible** | bool | `false` | Determines whether the Alert should be visible
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**width** | number | null | Fixed width of Alert (in pixels)
**iconName** | string | null | Specifies an icon name - check [Icon](?id=icon) component
**iconSize** | number | null | Specifies an icon size
**iconColor** | string | null | Specifies an icon color
**background** | string | null | Specifies an background color of component
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Add `style` properties for better customization
**requestClose** | function | null | Function which will be called on cross button click to close the alert

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/alert.png" style="margin:auto;width: 558px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleAlert.js */

<RSAlert
	visible={this.state.showAlert}
	iconName='MdFlight'
	background={Styles.turquoiseGradient}
	requestClose={this.closeAlert.bind(this)}>
	<p>Get ready your boarding pass! Boarding starts at 09:45AM.</p>
</RSAlert>
```

<br>
<br>

---

## Button

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**size** | string | `medium` | One of: `small`, `medium`, `large`
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**background** | string | null | Specifies an background color of component
**color** | string | null | Specifies an color of label
**fullWidth** | bool | `false` | Set width on 100% - it follow parent's width then
**value** | string | null | Text value of component
**iconName** | string | null | Specifies an icon name - check [Icon](?id=icon) component
**iconSize** | number | `18` | Specifies an icon size
**iconColor** | string | null | Specifies an icon color
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
**valueStyle** | object, array | null | Allows you to style label ex. `textTransform: uppercase;`
| | | | **Any other additional props will be passed down to `button` element (eg. onClick)**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/button.png" style="margin:auto;width: 241px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleButton.js */

/* Orange button */
<RSButton
	value='Button'
	background={Styles.orangeGradient}
	onClick={this.onClick.bind(this)}
/>

/* Red button with icon */
<RSButton
	value='Delete'
	iconName='FaTrash'
	iconSize={15}
	background={Styles.redColor}
	onClick={this.onClick.bind(this)}
/>
```

<br>
<br>

---

## Checkbox

You can pass all supported `<input type='checkbox' />` `props` as well as `props` listed below:

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**checked** | bool | `false` |
**value** | string, number | null | Defines a value associated with the component
**label** | string | null | Defines `<label />` element of component
**background** | string | null | Specifies an background color
**color** | string | null | Specifies an icon color
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
**onChange** | function | null | Function called on checkbox state change with args **value, checkedState, label**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/checkbox.png" style="margin:auto;width: 86px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleCheckbox.js */

/* Black un-checked Checkbox with label */
<RSCheckbox
	label='Label'
	value='checkbox1'
	background={Styles.blackGradient}
	onChange={this.onChange.bind(this)}
/>

/* Black checked Checkbox with label */
<RSCheckbox
	checked
	label='Label'
	value='checkbox2'
	background={Styles.blackGradient}
	onChange={this.onChange.bind(this)}
/>

/* Black checked, disabled Checkbox with label */
<RSCheckbox
	disabled
	checked
	label='Label'
	value='checkbox3'
	background={Styles.blackGradient}
	onChange={this.onChange.bind(this)}
/>
```

<br>
<br>

---

## Color Card

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | `Primary Color` | Text label with name of presented color
**color** | string | `Styles.primaryColor` | Defines a color value of the component

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/color-card.png" style="margin:auto;width: 281px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleColorCard.js */

/* Color Card - Mint Color */
<RSColorCard
	label='Mint'
	color={Styles.mintColor}
/>

/* Color Card - Gray Color */
<RSColorCard
	label='Gray'
	color={Styles.grayColor}
/>
```

<br>
<br>

---

## Form Label

You can pass all supported `<label />` `props` as well as `props` listed below:

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**id** | string | null | Defines `id` of `<input />` etc.
**className** | string | null | Add `className` on container of component

```reactjs
<RSFormLabel id={this.props.id}>
	Input Label
</RSFormLabel>
```

<br>
<br>

---

<br>
<br>

## Icon

You are able to use all supported icons from popular icon packs like **Font Awesome** and ** Material Design**.

List of icons:
- [Material Design](https://material.io/icons/)
- [Font Awesome](http://fontawesome.io/icons/)

Use their original name to get the icon you want. **For example: `FaTrash` or `MdError`**

*You need to have installed `react-icons` in your project to be able to use our `RSIcon` component. Check [install guide]() and install all required packages if you missed something at the beginning.*

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**name** | string | null | Specifies an icon name
**size** | number | `18` | Specifies an icon size
**color** | string | `Styles.primaryTextColor` | Specifies an icon color

```reactjs
<RSIcon
	name='MdError'
	size={26}
	color={Styles.redColor}
/>
```

<br>
<br>

---

<br>
<br>

## Input

You can pass all supported `<input />` `props` as well as `props` listed below:

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | null | Defines `<label />` element of component
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**text** | string | null | Text description below input
**textWithIcon** | string | null | Text description below input with `Icon` when used with `level` prop
**iconName** | string | null | Specifies an icon name - check [Icon](?id=icon) component
**iconSize** | number | `20` | Specifies an icon size
**iconOnRight** | bool | `false` | `Icon` inside of input is aligned to the right
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
**onChange** | function | null | Called on its value update, the value passed as an argument
| | | | **Any other additional props will be passed down to `input` element**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/input.png" style="margin:auto;width: 520px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleInput.js */

/* Input with Icon */
<RSInput
	iconName='FaCalendar'
	iconSize={14}
	placeholder='Value'
	type='text'
	onChange={this.onChange.bind(this)}
/>

/* Input with Label, Text information and set SUCCESS level */
<RSInput
	label='Input Label'
    level='success'
    text='Positive Message'
    placeholder='Value'
	type='text'
	onChange={this.onChange.bind(this)}
/>
```

<br>
<br>

---

## Label

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**text** | string | null | Text value of component
**background** | string | `Styles.primaryColor` | Specifies an background color of component
**color** | string | `Styles.primaryTextColor` | Specifies an color of label
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/label.png" style="margin:auto;width: 296px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleLabel.js */

/* Orange gradient on background */
<RSLabel
	text='Swift'
	background={Styles.orangeGradient}
/>

/* Fusion gradient on background */
<RSLabel
	text='ReactSymbols UI Kit Release'
	background={Styles.fusionGradient}
/>

/* Black gradient on background */
<RSLabel
	text='Admin'
	background={Styles.blackGradient}
/>
```

<br>
<br>

---

## Notification

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**value** | number | `0` | Defines a value presented in notification bullet
**background** | string | null | Specifies an background color of notification bullet
**color** | string | null | Specifies an color of number of notifications
**rounded** | number | `20` | `border-radius` of notification bullet in pixels
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/notification.png" style="margin:auto;width: 306px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleNotification.js */

/* Icon as content */
<RSNotification value={13}>
	<RSIcon
		name='FaInstagram'
		size={26}
		color={Styles.darkTextColor}
	/>
</RSNotification>

/* Label as content and Red bullet */
<RSNotification value={2} background={Styles.redGradient}>
	<RSLabel
		text='Messages'
		background={Styles.blueGradient}
	/>
</RSNotification>

/* Longer string and Black background */
<RSNotification value={18283} background={Styles.blackGradient}>
	<RSLabel
		text='Notification alert'
		background={Styles.orangeGradient}
	/>
</RSNotification>
```

<br>
<br>

---

## Progress Bar

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**fill** | number | `0` | Presenting width of filled bar in percentages
**label** | string | null | Value of text label placed above progress bar
**color** | string | null | Specifies an color of progress bar
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/progress-bar.png" style="margin:auto;width: 497px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleProgressBar.js */

<RSProgressBar
	label='Uploading...'
	fill={this.state.fill}
/>
```

<br>
<br>

---

<br>
<br>

## Radio

**For group of `Radio` component use `RadioGroup` - [check it](?id=radio-group)**

You can pass all supported `<input type='radio' />` `props` as well as `props` listed below:

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | null | Definition of `<label>` for the Radio component
**background** | string | null | Specifies an background color of component
**color** | string | null | Specifies an color of bullet when `checked`
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
| | | | **Any other props will be passed down to `radio input` element (eg. onChange)**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/radio.png" style="margin:auto;width: 97px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleRadioGroup.js */

/* Radio button with custom background */
<RSRadio
	value='radio1'
	label='Label 1'
	background={Styles.turquoiseGradient}
/>

/* Radio button with custom background and selected */
<RSRadio
	checked
	value='radio2'
	label='Label 2'
	background={Styles.turquoiseGradient}
/>

/* Radio button with custom background and disabled */
<RSRadio
	disabled
	value='radio3'
	label='Label 3'
	background={Styles.turquoiseGradient}
/>
```

<br>
<br>

---

## Radio Group

**Documentation for `Radio` component you can [find here](?id=radio)**

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**selectedValue** | string, number | null | Value of selected child - `Radio`
**onChange** | function | null | Called when an active radio element has been changed, with radio value as an argument
<br>

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/radio.png" style="margin:auto;width: 97px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleRadioGroup.js */

<RSRadioGroup
	selectedValue='radio2'
	onChange={this.onChange.bind(this)}
	name='radio-group'>

	<RSRadio
		value='radio1'
		label='Label 1'
		background={Styles.turquoiseGradient}
	/>
	<RSRadio
		value='radio2'
		label='Label 2'
		background={Styles.turquoiseGradient}
	/>
	<RSRadio
		disabled
		value='radio3'
		label='Label 3'
		background={Styles.turquoiseGradient}
	/>
</RSRadioGroup>
```

<br>
<br>

---

## Select

*You need to have installed `react-select` in your project to be able to use our `RSSelect` component. Check [install guide]() and install all required packages if you missed something at the beginning.*

You are still able to use all benefits of `react-select` (check documentation) but our component UI is currently made for standard use cases of `<Select>`. You can also pass image values into your `RSSelect` or change rounding of the image.

> **`<RSSelect />` will pass all `react-select` props** and for more info check [Select Option](?id=select-option).

<br>

## Select Option

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | null | Text value of component
**image** | string | null | Path to image file
**rounded** | number | `4` | `border-radius` of image in pixels
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/select.png" style="margin:auto;width: 368px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleSelect.js */

imageOption (option) {
	return (
		<RSSelectOption
			label={option.label}
			image={imageReq(option.imagePath)}
		/>
	)
}

<RSSelect
	value={this.state.values[1]}
	searchable={false}
	clearable={false}
	options={selectData}
	onChange={this.handleChangeSelect.bind(this, 1)}
	valueRenderer={this.imageOption}
	optionRenderer={this.imageOption}
/>
```

<br>
<br>

---

<br>
<br>

## Social Button

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**theme** | string | `light` | One of: `light`, `dark`
**iconName** | string | null | Specifies an icon name - check [Icon](?id=icon) component
**iconSize** | number | 16 | Specifies an icon size
**color** | string | null | Specifies an icon color
**background** | string | null | Specifies an background color of component
**rounded** | number | `18` | `border-radius` of button in pixels
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
| | | | **Any other props will be passed down to `a` element**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/social-button.png" style="margin:auto;width: 141px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleSocialButton.js */

<RSSocialButton
	iconName='FaTwitter'
	onClick={this.onClick.bind(this)}
/>

<RSSocialButton
	disabled
	iconName='FaPinterest'
	onClick={this.onClick.bind(this)}
/>

<RSSocialButton
	theme='dark'
	iconName='FaGooglePlus'
	onClick={this.onClick.bind(this)}
/>
```

<br>
<br>

---

## Switch

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**checked** | bool | false |
**value** | string, number | null | Defines a value associated with the component
**label** | string | null | Defines `<label />` element of component
**background** | string | null | Specifies an background color of component
**rounded** | number | `999` | `border-radius` of button in pixels
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
**onChange** | function | null | Called on switch state change, **label** and **boolean state** passed as function args

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/switch.png" style="margin:auto;width: 344px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleSwitch.js */

<RSSwitch
	checked
	label='Label'
	value='switch1'
	onChange={this.onChange.bind(this)}
	background={Styles.turquoiseGradient}
/>

<RSSwitch
	label='Label'
	value='switch2'
	onChange={this.onChange.bind(this)}
	background={Styles.redGradient}
/>

<RSSwitch
	checked
	rounded={0}
	label='Label'
	value='switch3'
	onChange={this.onChange.bind(this)}
	background={Styles.fusionGradient}
/>
```

<br>
<br>

---

## Textarea

You can pass all supported `<textarea />` `props` as well as `props` listed below:

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | null | Defines `<label />` element of component
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**text** | string | null | Text description below textarea
**textWithIcon** | string | null | Text description below textarea with `Icon` when used with `level` prop
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
**style** | object, array | null | Allows you to style component ex. `backgroundColor: red;`
**onChange** | function | null | Called on its value update, the value passed as an argument
| | | | **Any other additional props will be passed down to `textarea` element**

<div style="display: block; text-align: center;"><img src="http://docs.reactsymbols.com/images/textarea.png" style="margin:auto;width: 521px;"/></div>

```reactjs
/* Full real example of use you can find in examples/ExampleTextarea.js */

<RSTextarea
	id='textarea1'
	label='Textarea Label'
	type='text'
	placeholder='Everybody good? Plenty of slaves for my robot colony? - Interstellar'
	onChange={this.onChange.bind(this)}
/>

<RSTextarea
	id='textarea2'
	label='Textarea Label'
	level='danger'
	textWithIcon='Error Message'
	type='text'
	placeholder='Everybody good? Plenty of slaves for my robot colony? - Interstellar'
	onChange={this.onChange.bind(this)}
/>
```

<br>
<br>
