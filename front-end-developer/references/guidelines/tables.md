# Tables

## Text nowrap

- Ensure table rows remain on a single line, even on small devices.
- When using Bootstrap, add the text-nowrap class to each <td> element within the <tbody> section.

## Text nowrap

- Ensure table rows remain on a single line, even on small devices.
- When using Bootstrap, add the `text-nowrap` class to each `<td>` element within the `<tbody>` section.

## Columns

### Preferred structure

- First column: `#` (avatar or identifier)
- Last column: `Actions`

### Actions column rules

- Must contain: **View**, **Update**
- Avoid more than two inline actions
- Do not use icons in buttons

## Examples

> Note: The following examples are from the Tabler framework.

### #

#### Text

``` html
<td>
    <a href="/applicants/230">
        <span class="avatar avatar-2 bg-blue-lt text-blue-lt-fg">MM</span>
    </a>
</td>
```

#### Avatar

``` html
<td>
  <a href="/vpss/1">
    <span class="avatar avatar-2">
      <svg class="icon icon-tabler icons-tabler-outline icon-tabler-device-imac" viewBox="0 0 24 24" fill="none" height="24" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" width="24" xmlns="http://www.w3.org/2000/svg">
        <path d="M0 0h24v24H0z" fill="none" stroke="none"></path>
        <path d="M3 4a1 1 0 0 1 1 -1h16a1 1 0 0 1 1 1v12a1 1 0 0 1 -1 1h-16a1 1 0 0 1 -1 -1v-12z"></path>
        <path d="M3 13h18"></path>
        <path d="M8 21h8"></path>
        <path d="M10 17l-.5 4"></path>
        <path d="M14 17l.5 4"></path>
      </svg>
    </span>
  </a>
</td>
```

### Actions

``` html
<td>
    <div class="btn-list flex-nowrap">
        <a class="btn" href="/vpss/1">View</a>
        <a class="btn" href="/vpss/1/update">Update</a>
    </div>
</td>
```