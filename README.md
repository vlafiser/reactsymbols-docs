# Documentation

Welcome in offical documentation of `ReactSymbols React UI Kit` which is made for `ReactJS` applications and you can easily use each and all of the component in your project. We are pushing it with lot of predefined colors so it's perfectly fit for *prototyping* of your IU for your new feature of page.

- [Website](http://www.reactsymbols.com)
- [Sketch resources](http://symbols.janlosert.com)

Support: [react@vlastimilfiser.com](mailto:react@vlastimilfiser.com)

<br>

**PLANNED UPDATES:**
- **Typescript support** `NEW`
- Adding support of SASS files and be able to change color variables to make it fit with your brand by one line code of CSS color.
- Adding more components (different types of buttons, dropdown,...)

<br>

**CHANGELOG:**

`1.0.0` [22.11.2017] - Initial release version

<br>

**STRUCTURE OF FOLDER:**
<img src="http://docs.reactsymbols.com/images/folder-structure.png" style="display:block;width: 186px;margin-top:20px;"/>

<br>

---

<br>

# **Setup**

## Run our Demo app

<iframe width="560" height="315" src="https://www.youtube.com/embed/4li6B3tdh1E" frameborder="0" allowfullscreen></iframe>

<br>

**1)** In Terminal go to the folder where our `ReactSymbolsDemoApp` is placed
```
cd ./path/ReactSymbolsKit/ReactSymbolsDemoApp
```

**2)** Install dependencies via NPM
```
npm install
```

**3)** Then start your localhost and build our demo app easily by
```
npm start
```

**4)** 🎉 You can see all the ReactSymbols elements together in real app

----

## Use in your project

<iframe width="560" height="315" src="https://www.youtube.com/embed/Hv6UgTvFHak" frameborder="0" allowfullscreen></iframe>

**1)** Move `react-symbols-kit` folder you downloaded into your your project folder.

**2)** Install local module with react-symbols-kit (It will also download all required dependencies)
```bash
	npm install <your-path>/react-symbols-kit
```

**3)** Link the stylesheet files and define which components you like to import:
```javascript
import 'react-symbols-kit/ReactSymbolsKit.css'
import { RSButton } from 'react-symbols-kit'
```

**4)** Let's call the component you want to use! All available props are available separately for each component below in this documentation. For example:
```javascript
<RSButton value='Your first RSButton' />
```

**4)** 🎉 You made first ReactSymbols component!

**If you love TypeScript, you will love ReactSymbolsKit as well ❤️. We do have declared TypeScript bindings for super easy autocompletion feature in your IDE.** 😍

<br>

-----

<br>

# **Components**

List of available components:
- [RSAlert](?id=RSAlert)
- [RSButton](?id=RSButton)
- [RSCheckbox](?id=RSCheckbox)
- [RSColorCard](?id=RSColorCard)
- [RSFormLabel](?id=RSFormLabel)
- [RSIcon](?id=RSIcon)
- [RSInput](?id=RSInput)
- [RSLabel](?id=RSLabel)
- [RSNotification](?id=RSNotification)
- [RSProgressBar](?id=RSProgressBar)
- [RSRadio](?id=RSRadio)
- [RSRadioGroup](?id=RSRadioGroup)
- [RSSelect](?id=RSSelect)
- [RSSelectOption](?id=RSSelectOption)
- [RSSocialButton](?id=RSSocialButton)
- [RSSwitch](?id=RSSwitch)
- [RSTextarea](?id=RSTextarea)

-----

## RSAlert

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
**requestClose** | func | null | Function which will be called on cross button click to close the alert

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

## RSButton

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
| | | **Any other additional props will be passed down to `button` element (eg. onClick)**

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

## RSCheckbox

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
**onChange** | func | null | Function called on checkbox state change with args **value, checkedState, label**

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

## RSColorCard

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

## RSFormLabel

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**id** | string | null | Defines `id` of `<input />` etc.
**className** | string | null | Add `className` on container of component
| | | **Any other additional props will be passed down to `label` element (eg. name)**

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

## RSIcon

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

## RSInput

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
| | | **Any other additional props will be passed down to `input` element**

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

## RSLabel

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

## RSNotification

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

## RSProgressBar

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

## RSRadio

**For group of `RSRadio` component use `RSRadioGroup` - [check it](?id=rsradiogroup)**

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**PROP** | **TYPE** | **DEFAULT** | **DESCRIPTION**
**label** | string | null | Definition of `<label>` for the Radio component
**background** | string | null | Specifies an background color of component
**color** | string | null | Specifies an color of bullet when `checked`
**disabled** | bool | `false` | Determines whether the component should be disabled
**className** | string | null | Add `className` on container of component
| | | **Any other props will be passed down to `radio input` element (eg. onChange)**

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

## RSRadioGroup

**Documentation for `RSRadio` component you can [find here](?id=rsradio)**

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

## RSSelect

Our component is working with `react-select` ([documentation](http://jedwatson.github.io/react-select/)) which means that you can use all available functionality of `react-select`.
Our component `RSSelect` is currently made for standard use cases of `<Select>`. You can also pass image values into your `RSSelect` or change rounding of the image.

> **`<RSSelect />` will pass down all `react-select` props** - for more info check [RSSelectOption](?id=rsselectoption).


## RSSelectOption

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

## RSSocialButton

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
| | | **Any other props will be passed down to `a` element**

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

## RSSwitch

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
**onChange** | func | null | Called on switch state change, **label** and **boolean state** passed as function args

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

## RSTextarea

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
| | | **Any other additional props will be passed down to `textarea` element**

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
