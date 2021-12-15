# MMM-VUB-Resto

A Module for [MagicMirror](https://github.com/MichMich/MagicMirror) designed to
display the menu of the restaurant at the Vrije Universiteit Brussel.

The data are retrieved from http://call-cc.be/files/vub-resto/etterbeek.en.json

## Sample

![alt text](https://github.com/OscarVsp/MMM-VUB-Resto/raw/main/sample.jpg "Example")

## Installation

**Clone the repository into MagicMirror/modules directory**
```bash
cd ~/MagicMirror/modules
git clone https://github.com/OscarVsp/MMM-VUB-Resto.git
```

**Install the dependencies**
```bash
cd ~/MagicMirror/modules/MMM-VUB-Resto
npm install
```

### Config

**Basic Example:**

```jsonc
{
  module: 'MMM-VUB-Resto',
  position: 'bottom_left',
  header: 'Restaurant menu of the day'
},
```

**Hide some meal:**

```jsonc
{
  module: 'MMM-VUB-Resto',
  position: 'bottom_left',
  header: 'Restaurant menu of the day',
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
        <br><b>Default:</b> <code>3,600,000</code> => 1 hour
      </td>
    </tr>
    <tr>
      <td><code>headerIcon</code></td>
      <td>The Icon for your Header
        <br><b>Type:</b> <code>string</code> <a href="https://fontawesome.com/icons?d=gallery">any FontAwesome Icon</a>
        <br><b>Default:</b> <code>"fa-utensils"</code> 
      </td>
    </tr>
    <tr>
      <td><code>hides</code></td>
      <td>The values you want to hide
        <br><b>Type:</b> <code>array</code>
        <br><b>Possible values:</b> <code>"Soup"</code>,<code>"Menu 1"</code>,<code>"Menu 2"</code>,<code>"Wok"</code>,<code>"Veggie"</code> and <code>"Pasta"</code>
        <br><b>Default:</b> <code>[]</code> 
      </td>
    </tr>
  </tbody>
</table>

## Attribution

Strongly based on MMM-Json from Daniel Habenicht
https://github.com/DanielHabenicht/MMM-json
