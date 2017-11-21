# About ReactSymbols 

#### Files naming
Naming of all Components and their SASS files starts with `RS` for example `RSButton.js` or `RSButton.scss`. We don't want to create mess into your app or fight names of your existing files. It's also good for identification of code from ReactSymbols UI Kit.

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

<div style="display: block; text-align: center;"><img src="http://localhost:3000/images/alert.png" style="margin:auto;width: 558px;"/></div>

```reactjs
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

<div style="display: block; text-align: center;"><img src="http://localhost:3000/images/button.png" style="margin:auto;width: 241px;"/></div>

```reactjs
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

<div style="display: block; text-align: center;"><img src="http://localhost:3000/images/checkbox.png" style="margin:auto;width: 86px;"/></div>

```reactjs
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

<div style="display: block; text-align: center;"><img src="http://localhost:3000/images/color-card.png" style="margin:auto;width: 281px;"/></div>

```reactjs
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

<div style="display: block; text-align: center;"><img src="http://localhost:3000/images/input.png" style="margin:auto;width: 520px;"/></div>

```reactjs
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

<br>
<br>

## Label

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**text** | string | null | Text value of presented Label component
**background** | string | null | Background color of the Label component
**color** | string | null | Text color of the Label component
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Input customization

<br>

#### Example of use:

```reactjs
<SKLabel
  text='Administrator'
  background={Styles.redGradient}
/>
```

<br>
<br>

---

<br>
<br>

## Notification

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**value** | number | 0 | The value of Notification component
**background** | string | null | Background color of the Notification indicator
**color** | string | null | Color of the number of Notification indicator
**rounded** | number | null | `border-radius` of Notification indicator in pixels
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better customization

<br>

#### Example of use:

```reactjs
<SKNotification items={2}>
  <SKIcon
    name='instagram'
    size={26}
    color={colors.darkTextColor}
  />
</SKNotification>
```

<br>
<br>

---

<br>
<br>

## Progress Bar

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**fill** | number | 0 | Width of fill of ProgressBar in percentages
**label** | string | null | Definition of `<label>` for the component
**className** | string | null | Your own `className` for better customization

<br>

#### Example of use:

```reactjs
<SKProgressBar
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

> **Correct use of `Radio` component is in `RadioGroup` component - [check it](components.md?id=radio-group) for real example**

You can also pass all props supported defaultly by `<input type='radio'/>` - check ReactJS documentation

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**value** | string, number | null | Defines a value associated with the component
**label** | string | null | Definition of `<label>` for the Radio component
**checked** | bool | false | 
**disabled** | bool | false | Determines whether the Radio should be disabled
**className** | string | null | Your own `className` for better customization

<br>

#### Example of use:

```reactjs
<SKRadio
  value='radio1'
  label='Radio 1'
/>
```

<br>
<br>

---

<br>
<br>

## Radio Group

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**selectedValue** | string, number | null | Value of selected child `Radio` element
**onChange** | func | null |

<br>

#### Example of use:

```reactjs
<SKRadioGroup selectedValue='radio1' onChange={this.onChange.bind(this)} name='radio-group'>
  <SKRadio value='radio1' label='Radio 1' />
  <SKRadio value='radio2' label='Radio 2' />
  <SKRadio value='radio3' label='Radio 3' disabled={true} />
</SKRadioGroup>
```

<br>
<br>

---

<br>
<br>

## Select

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**className** | string | null | Your own `className` for better customization

**You can pass all props supported by `React-Select` component - check their documentation for all available settings**

<br>

#### Example of use:

```reactjs
<SKSelect
  name='countries-select'
  value={this.state.value}
  searchable={false}
  clearable={false}
  options={options}
  onChange={this.handleChange.bind(this)}
  className='custom-select-class'
  valueRenderer={this.renderRoundedValue}
  optionRenderer={this.renderRoundedValue}
/>
```

<br>
<small>`Select` component is build on `React-Select` component. Styles are made specifically for examples you can see below (other functionality of `React-Select` may not work properly with our styles)</small>

<br>
<br>

---

<br>
<br>

## Social Button

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**theme** | string, number | `light` | One of: `light`, `dark`
**iconName** | string | null | Specifies an icon name - check [Icon](components.md?id=icon) component for all options
**iconSize** | number | 16 | Specifies an icon size
**iconColor** | string | null | Specifies an icon color
**rounded** | number | null | `border-radius` of Social Button indicator in pixels
**disabled** | bool | false | Determines whether the Social Button should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Social Button customization

<br>

#### Example of use:

```reactjs
<SKSocialButton
  iconName='twitter'
  iconColor={Styles.greenColor}
  iconSize={10}
  onClick={this.onClick.bind(this)}
/>
```

<br>
<br>

---

<br>
<br>

## Switch

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**checked** | bool | false | 
**value** | string, number | null | Defines a value associated with the component
**label** | string | null | Definition of `<label>` for the Switch component
**rounded** | number | null | `border-radius` of Social Button indicator in pixels
**disabled** | bool | false | Determines whether the Social Button should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Social Button customization

<br>

#### Example of use:

```reactjs
<SKSwitch
  value='notification-switch'
  label='Turn on notificatons'
  checked={true}
  disabled={false}
  onChange={this.onChange.bind(this)}
/>
```

<br>
<br>

---

<br>
<br>

## Textarea

You can also pass all `<textarea>` props - check ReactJS documentation

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**id** | string | null | Defines HTML `id` property of the component
**label** | string | null | Definition of `<label>` for the component
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**text** | string | null | Text description below Textarea
**textWithIcon** | string | null | Text description below Textarea will include `Icon` when used with `level` prop
**disabled** | bool | false | Determines whether the component should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better customization

<br>

#### Example of use:

```reactjs
<SKTextarea
  id='textarea'
  textWithIcon='Your text information below textarea'
  placeholder='Your Placeholder'
  type='text'
  onChange={this.onChange.bind(this)}
/>
```

<br>
<br>