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

### Table

``` html
<div class="col-12">
  <div class="card">
    <div class="table-responsive">
      <table class="table table-vcenter table-nowrap card-table">
        <thead>
          <tr>
            <th></th>
            <th>Name</th>
            <th class="w-1">Actions</th>
          </tr>
        </thead>
        <tbody>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/1">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>AFGHANISTAN</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/1">View</a>
                <a class="btn" href="/nationalities/1/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/2">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ALBANIA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/2">View</a>
                <a class="btn" href="/nationalities/2/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/3">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ALGERIA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/3">View</a>
                <a class="btn" href="/nationalities/3/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/4">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ANGOLA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/4">View</a>
                <a class="btn" href="/nationalities/4/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/5">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ANGUILLA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/5">View</a>
                <a class="btn" href="/nationalities/5/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/6">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ANTIGUA AND BARBUDA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/6">View</a>
                <a class="btn" href="/nationalities/6/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/7">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ARGENTINA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/7">View</a>
                <a class="btn" href="/nationalities/7/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/8">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ARMENIA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/8">View</a>
                <a class="btn" href="/nationalities/8/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/9">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>ARUBA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/9">View</a>
                <a class="btn" href="/nationalities/9/update">Update</a>
              </div>
            </td>
          </tr>
          <!-- Row -->
          <tr>
            <td>
              <a href="/nationalities/10">
                <span class="avatar avatar-2">
                  <!-- avatar icon -->
                </span>
              </a>
            </td>
            <td>AUSTRALIA</td>
            <td>
              <div class="btn-list flex-nowrap">
                <a class="btn" href="/nationalities/10">View</a>
                <a class="btn" href="/nationalities/10/update">Update</a>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="card-footer">
      <div class="d-flex justify-content-between">
        <div>
          <div class="btn-list">
            <a class="btn btn-primary disabled d-sm-none btn-icon" href="#">
              <!-- arrow left icon -->
            </a>
            <a class="btn btn-primary disabled d-none d-sm-inline-block" href="#">
              <!-- arrow left icon -->
              Previous
            </a>
          </div>
        </div>
        <div>
          <div class="btn-list">
            <a class="btn btn-primary d-sm-none btn-icon" href="/nationalities/?page=2">
              <!-- arrow right icon -->
            </a>
            <a class="btn btn-primary d-none d-sm-inline-block" href="/nationalities/?page=2">
              <!-- arrow right icon -->
              Next
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```