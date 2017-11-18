
# **Information**

# **Getting started**

# **Components**

## Alert

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**visible** | bool | false | Determines whether the Button should be visible
**level** | string | info | One of: `success`, `danger`, `warning`, `info`
**width** | string | null | Fixed width of alert in **pixels** (default is 100% - following parent's width)
**iconName** | string | null | Specifies an icon name - check [Icon](components.md?id=icon) component for all options
**iconSize** | number | null | Specifies an icon size
**iconColor** | string | null | Specifies an icon color
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better customization

<br>

#### Example of use:

```reactjs
<SKAlert
  visible={this.state.showAlert}
  level='danger'
  requestClose={this.requestAlertClose.bind(this)}
  className='alertMargin'>
  <p>Success! This is positive Alert.</p>
</SKAlert>
```

<br>
<br>

---

<br>
<br>

## Button

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**size** | string | medium | One of: `small`, `medium`, `large`
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**background** | string | null | Background color of the Button component
**color** | string | null | Label color of the Button component
**fullWidth** | bool | false | It follows width of parent it it's `true`
**value** | string | null | Text value of Button component
**iconName** | string | null | Specifies an icon name - check [Icon](components.md?id=icon) component for all options
**iconSize** | number | 18 | Specifies an icon size
**iconColor** | string | null | Specifies an icon color
**disabled** | bool | false | Determines whether the Button should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Button customization
**valueStyle** | object, array | null | Your own `style` properties for better text value Button customization

<br>

#### Example of use:

```reactjs
<SKButton
  name='button-alert'
  value='Open Alert'
  onClick={this.openAlert.bind(this)}
/>
```

<br>
<br>

---

<br>
<br>

## Checkbox

You can pass all `Checkbox` props - check ReactJS documentation

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**checked** | bool | false | 
**value** | string, number | null | Defines a value associated with the component
**label** | string | null | Definition of `<label>` for the Checkbox component
**iconColor** | string | null | Specifies an icon color
**disabled** | bool | false | Determines whether the Button should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Button customization

<br>

#### Example of use:

```reactjs
<SKCheckbox
  checked={true}
  label='By check of this box you accept with Privacy Policy'
  value='checkbox1'
  name='checkbox1'
  onChange={this.onChange.bind(this)}
/>
```

<br>
<br>

---

<br>
<br>

## Color Card

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**label** | string | Color | Text description label of ColorCard component
**color** | string | #000000 | Defines a color value of the ColorCard component

<br>

#### Example of use:

```reactjs
<SKColorCard
  label='Red color'
  color={Styles.redColor}
/>
```

<br>
<br>

---

<br>
<br>

## Form Label

You can also pass all `<label>` props - check ReactJS documentation

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**id** | string | null | Defines HTML `id` property of FormLabel component
**className** | string | null | Your own `className` for better customization

<br>

#### Example of use:

```reactjs
<SKFormLabel
  id={this.props.id}>
  This is label
</SKFormLabel>
```

<br>
<br>

---

<br>
<br>

## Icon

#### ⏱ COMING SOON

<br>
<br>

---

<br>
<br>

## Input

You can also pass all `<input>` props - check ReactJS documentation

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**id** | string | null | Defines HTML `id` property of Input component
**label** | string | null | Definition of `<label>` for the Checkbox component
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**text** | string | null | Text description below input
**textWithIcon** | string | null | Text description below input will include `Icon` when used with `level` prop
**type** | string | text | Define type of input (`text`, `password`...)
**iconName** | string | null | Specifies an icon name - check [Icon](components.md?id=icon) component for all options
**iconSize** | number | 18 | Specifies an icon size
**iconOnRight** | bool | false | `Icon` in input will be aligned to the right
**valid** | bool | false | Will apply `success` color level on the Input component
**invalid** | bool | false | Will apply `danger` color level on the Input component
**disabled** | bool | false | Determines whether the Input should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better Input customization

<br>

#### Example of use:

```reactjs
<SKInput
  valid={true}
  type='text'
  textWithIcon='This is little text information'
  id='input1'
  placeholder='Your Placeholder'
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

<br>

<span class="tab-title">PROP</span> | <span class="tab-title">TYPE</span> | <span class="tab-title">DEFAULT</span> | <span class="tab-title">DESCRIPTION</span>
:--- | :--- | :--- | :---
**id** | string | null | Defines HTML `id` property of the component
**label** | string | null | Definition of `<label>` for the component
**level** | string | null | One of: `success`, `danger`, `warning`, `info`
**text** | string | null | Text description below Textarea
**textWithIcon** | string | null | Text description below Textarea will include `Icon` when used with `level` prop
**valid** | bool | false | Will apply `success` color level on the component
**invalid** | bool | false | Will apply `danger` color level on the component
**disabled** | bool | false | Determines whether the component should be disabled
**className** | string | null | Your own `className` for better customization
**style** | object, array | null | Your own `style` properties for better customization

<br>

#### Example of use:

```reactjs
<SKTextarea
  id='textarea'
  valid={true}
  textWithIcon='Your text information below textarea'
  placeholder='Your Placeholder'
  type='text'
  onChange={this.onChange.bind(this)}
/>
```

<br>
<br>