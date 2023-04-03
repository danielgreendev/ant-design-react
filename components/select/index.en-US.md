---
category: Components
group: Data Entry
title: Select
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*zo76T7KQx2UAAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*5oPiTqPxGAUAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
---

Select component to select value from options.

## When To Use

- A dropdown menu for displaying choices - an elegant alternative to the native `<select>` element.
- Utilizing [Radio](/components/radio/) is recommended when there are fewer total options (less than 5).

## Examples

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">Basic Usage</code>
<code src="./demo/search.tsx">Select with search field</code>
<code src="./demo/multiple.tsx">multiple selection</code>
<code src="./demo/size.tsx">Sizes</code>
<code src="./demo/option-label-prop.tsx">Custom selection render</code>
<code src="./demo/search-sort.tsx">Search with sort</code>
<code src="./demo/tags.tsx">Tags</code>
<code src="./demo/optgroup.tsx">Option Group</code>
<code src="./demo/coordinate.tsx">coordinate</code>
<code src="./demo/search-box.tsx">Search Box</code>
<code src="./demo/label-in-value.tsx">Get value of selected item</code>
<code src="./demo/automatic-tokenization.tsx">Automatic tokenization</code>
<code src="./demo/select-users.tsx">Search and Select Users</code>
<code src="./demo/suffix.tsx" debug>Suffix</code>
<code src="./demo/custom-dropdown-menu.tsx">Custom dropdown</code>
<code src="./demo/hide-selected.tsx">Hide Already Selected</code>
<code src="./demo/bordered.tsx">Bordered-less</code>
<code src="./demo/custom-tag-render.tsx">Custom Tag Render</code>
<code src="./demo/responsive.tsx">Responsive maxTagCount</code>
<code src="./demo/big-data.tsx">Big Data</code>
<code src="./demo/status.tsx">Status</code>
<code src="./demo/placement.tsx">Placement</code>
<code src="./demo/debug.tsx" debug>4.0 Debug</code>
<code src="./demo/render-panel.tsx" debug>\_InternalPanelDoNotUseOrYouWillBeFired</code>
<code src="./demo/option-label-center.tsx" debug>Options label Centered</code>

## API

```tsx
<Select>
  <Option value="lucy">lucy</Option>
</Select>
```

### Select props

| Property | Description | Type | Default | Version |
| --- | --- | --- | --- | --- |
| allowClear | Show clear button | boolean | false |  |
| autoClearSearchValue | Whether the current search will be cleared on selecting an item. Only applies when `mode` is set to `multiple` or `tags` | boolean | true |  |
| autoFocus | Get focus by default | boolean | false |  |
| bordered | Whether has border style | boolean | true |  |
| clearIcon | The custom clear icon | ReactNode | - |  |
| defaultActiveFirstOption | Whether active first option by default | boolean | true |  |
| defaultOpen | Initial open state of dropdown | boolean | - |  |
| defaultValue | Initial selected option | string \| string\[] \| <br />number \| number\[] \| <br />LabeledValue \| LabeledValue\[] | - |  |
| disabled | Whether disabled select | boolean | false |  |
| popupClassName | The className of dropdown menu | string | - | 4.23.0 |
| dropdownMatchSelectWidth | Determine whether the dropdown menu and the select input are the same width. Default set `min-width` same as input. Will ignore when value less than select width. `false` will disable virtual scroll | boolean \| number | true |  |
| dropdownRender | Customize dropdown content | (originNode: ReactNode) => ReactNode | - |  |
| dropdownStyle | The style of dropdown menu | CSSProperties | - |  |
| fieldNames | Customize node label, value, options field name | object | { label: `label`, value: `value`, options: `options` } | 4.17.0 |
| filterOption | If true, filter options by input, if function, filter options against it. The function will receive two arguments, `inputValue` and `option`, if the function returns `true`, the option will be included in the filtered set; Otherwise, it will be excluded | boolean \| function(inputValue, option) | true |  |
| filterSort | Sort function for search options sorting, see [Array.sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)'s compareFunction | (optionA: Option, optionB: Option) => number | - | 4.9.0 |
| getPopupContainer | Parent Node which the selector should be rendered to. Default to `body`. When position issues happen, try to modify it into scrollable content and position it relative. [Example](https://codesandbox.io/s/4j168r7jw0) | function(triggerNode) | () => document.body |  |
| labelInValue | Whether to embed label in value, turn the format of value from `string` to { value: string, label: ReactNode } | boolean | false |  |
| listHeight | Config popup height | number | 256 |  |
| loading | Indicate loading state | boolean | false |  |
| maxTagCount | Max tag count to show. `responsive` will cost render performance | number \| `responsive` | - | responsive: 4.10 |
| maxTagPlaceholder | Placeholder for not showing tags | ReactNode \| function(omittedValues) | - |  |
| maxTagTextLength | Max tag text length to show | number | - |  |
| menuItemSelectedIcon | The custom menuItemSelected icon with multiple options | ReactNode | - |  |
| mode | Set mode of Select | `multiple` \| `tags` | - |  |
| notFoundContent | Specify content to show when no result matches | ReactNode | `Not Found` |  |
| open | Controlled open state of dropdown | boolean | - |  |
| optionFilterProp | Which prop value of option will be used for filter if filterOption is true. If `options` is set, it should be set to `label` | string | `value` |  |
| optionLabelProp | Which prop value of option will render as content of select. [Example](https://codesandbox.io/s/antd-reproduction-template-tk678) | string | `children` |  |
| options | Select options. Will get better perf than jsx definition | { label, value }\[] | - |  |
| placeholder | Placeholder of select | ReactNode | - |  |
| placement | The position where the selection box pops up | `bottomLeft` `bottomRight` `topLeft` `topRight` | bottomLeft |  |
| removeIcon | The custom remove icon | ReactNode | - |  |
| searchValue | The current input "search" text | string | - |  |
| showArrow | Whether to show the drop-down arrow | boolean | true(for single select), false(for multiple select) |  |
| showSearch | Whether select is searchable | boolean | single: false, multiple: true |  |
| size | Size of Select input | `large` \| `middle` \| `small` | `middle` |  |
| status | Set validation status | 'error' \| 'warning' | - | 4.19.0 |
| suffixIcon | The custom suffix icon | ReactNode | - |  |
| tagRender | Customize tag render, only applies when `mode` is set to `multiple` or `tags` | (props) => ReactNode | - |  |
| tokenSeparators | Separator used to tokenize, only applies when `mode="tags"` | string\[] | - |  |
| value | Current selected option (considered as a immutable array) | string \| string\[] \| <br />number \| number\[] \| <br />LabeledValue \| LabeledValue\[] | - |  |
| virtual | Disable virtual scroll when set to false | boolean | true | 4.1.0 |
| onBlur | Called when blur | function | - |  |
| onChange | Called when select an option or input value change | function(value, option:Option \| Array&lt;Option>) | - |  |
| onClear | Called when clear | function | - | 4.6.0 |
| onDeselect | Called when an option is deselected, param is the selected option's value. Only called for `multiple` or `tags`, effective in multiple or tags mode only | function(value: string \| number \| LabeledValue) | - |  |
| onDropdownVisibleChange | Called when dropdown open | function(open) | - |  |
| onFocus | Called when focus | function | - |  |
| onInputKeyDown | Called when key pressed | function | - |  |
| onMouseEnter | Called when mouse enter | function | - |  |
| onMouseLeave | Called when mouse leave | function | - |  |
| onPopupScroll | Called when dropdown scrolls | function | - |  |
| onSearch | Callback function that is fired when input changed | function(value: string) | - |  |
| onSelect | Called when an option is selected, the params are option's value (or key) and option instance | function(value: string \| number \| LabeledValue, option: Option) | - |  |

> Note, if you find that the drop-down menu scrolls with the page, or you need to trigger Select in other popup layers, please try to use `getPopupContainer={triggerNode => triggerNode.parentElement}` to fix the drop-down popup rendering node in the parent element of the trigger .

### Select Methods

| Name    | Description  | Version |
| ------- | ------------ | ------- |
| blur()  | Remove focus |         |
| focus() | Get focus    |         |

### Option props

| Property  | Description                          | Type             | Default | Version |
| --------- | ------------------------------------ | ---------------- | ------- | ------- |
| className | The additional class to option       | string           | -       |         |
| disabled  | Disable this option                  | boolean          | false   |         |
| title     | `title` attribute of Select Option   | string           | -       |         |
| value     | Default to filter with this property | string \| number | -       |         |

### OptGroup props

| Property | Description | Type                    | Default | Version |
| -------- | ----------- | ----------------------- | ------- | ------- |
| key      | Group key   | string                  | -       |         |
| label    | Group label | string \| React.Element | -       |         |

## Design Token

<ComponentTokenTable component="Select"></ComponentTokenTable>

## FAQ

### Why sometime search will show 2 same option when in `tags` mode?

It's caused by option with different `label` and `value`. You can use `optionFilterProp="label"` to change filter logic instead.

### When I click elements in dropdownRender, the select dropdown will not be closed?

You can control it by `open` prop: [codesandbox](https://codesandbox.io/s/ji-ben-shi-yong-antd-4-21-7-forked-gnp4cy?file=/demo.js).

### I don't want dropdown close when click inside `dropdownRender`?

Select will close when it lose focus. You can prevent event to handle this:

```tsx
<Select
  dropdownRender={() => (
    <div
      onMouseDown={(e) => {
        e.preventDefault();
        e.stopPropagation();
      }}
    >
      Some Content
    </div>
  )}
/>
```

### Why sometime customize Option cause scroll break?

Virtual scroll internal set item height as `24px`. You need to adjust `listItemHeight` when your option height is less and `listHeight` config list container height:

```tsx
<Select listItemHeight={10} listHeight={250} />
```

Note: `listItemHeight` and `listHeight` are internal props. Please only modify when necessary.

### Why a11y test report missing `aria-` props?

Select only create a11y auxiliary node when operating on. Please open Select and retry. For `aria-label` & `aria-labelledby` miss warning, please add related prop to Select with your own requirement.

Default virtual scrolling will create a mock element to simulate an accessible binding. If a screen reader needs to fully access the entire list, you can set `virtual={false}` to disable virtual scrolling and the accessibility option will be bound to the actual element.