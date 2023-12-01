# ReactHTMLTableToExcel

Provides a client side generation of Excel (.xls) file from HTML table element.

---

No additional dependencies

---

## Installation

```
npm install --save export-html-table-to-excel
```

## Features

- Download HTML table as Excel file in .xls format
- No server side code
- Set desired .xls filename and sheet
- Set desired class name and id for styling
- Supported IE 11

## Options

A list of available properties can be found below. These must be passed to the containing `ReactHTMLTableToExcel` component.

| Property       | Type      | Description                                          |
| -------------- | --------- | ---------------------------------------------------- |
| **table**      | _string_  | ID attribute of HTML table element.                  |
| **filename**   | _string_  | Name of Excel file.                                  |
| **sheet**      | _string_  | Name of Excel sheet.                                 |
| **id**         | _string_  | ID attribute of button element.                      |
| **className**  | _string_  | Class attribute of button element.                   |
| **buttonText** | _string_  | Button text.                                         |
| **children**   | _element_ | Child elements to render instead of the button text. |

## Example

```javascript
import React, { Component } from "react";
import ReactHTMLTableToExcel from "export-html-table-to-excel";

class Test extends Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <ReactHTMLTableToExcel
          id="test-table-xls-button"
          className="download-table-xls-button"
          table="table-to-xls"
          filename="tablexls"
          sheet="tablexls"
          buttonText="Download as XLS"
        />
        <table id="table-to-xls">
          <tr>
            <th>Firstname</th>
            <th>Lastname</th>
            <th>Age</th>
          </tr>
          <tr>
            <td>Jill</td>
            <td>Smith</td>
            <td>50</td>
          </tr>
          <tr>
            <td>Eve</td>
            <td>Jackson</td>
            <td>94</td>
          </tr>
        </table>
      </div>
    );
  }
}

export default Test;
```
