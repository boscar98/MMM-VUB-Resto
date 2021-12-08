# MMM-VUB-Resto

A Module for [MagicMirror](https://github.com/MichMich/MagicMirror) designed to
display the menu of the vub restaurant.

The data are retrieved from http://call-cc.be/files/vub-resto/etterbeek.en.json

## Sample

![alt text](https://github.com/OscarVsp/MMM-VUB-Resto/raw/main/sample.jpg "Example")

## Installation

```bash
#  Clone the repository into MagicMirror/modules directory and install the dependencies
cd ./modules
git clone https://github.com/OscarVsp/MMM-VUB-Resto.git
cd /MMM-VUB-Resto
npm install
```

2. Create an entry in 'config/config.js' with your url and any config options.

### Sample

**Basic Example:**

```jsonc
{
  module: 'MMM-VUB-Resto',
  position: 'bottom_left',
},
```

**Hide some meal:**

```jsonc
{
  module: 'MMM-VUB-Resto',
  position: 'bottom_left',
  config: {
    hide: ["Veggie"]
  }
},
```

## Configuration

<table width="100%">
  <thead>
    <tr>
      <th>Property</th>
      <th width="100%">Description</th>
    </tr>
  <thead>
  <tbody>
    <tr>
      <td><code>refreshInterval</code></td>
      <td>The interval with which the url is queried and your values are updated.
        <br><b>Type:</b> <code>int</code> (seconds)
        <br><b>Default:</b> <code>6000000</code> => 5 minutes
      </td>
    </tr>
    <tr>
      <td><code>headerIcon</code></td>
      <td>The Icon for your Header
        <br><b>Type:</b> <code>string</code> <a href="https://fontawesome.com/icons?d=gallery">any FontAwesome Icon</a>
        <br><b>Default:</b> <code></code> (none)
      </td>
    </tr>
    <tr>
      <td><code>hides</code></td>
      <td>The values you want to hide
        <br><b>Type:</b> <code>array</code>
        <br><b>Default:</b> <code>[]</code> 
      </td>
    </tr>
  </tbody>
</table>

## Attribution

Strongly based on MMM-Json from Daniel Habenicht
https://github.com/DanielHabenicht/MMM-json
