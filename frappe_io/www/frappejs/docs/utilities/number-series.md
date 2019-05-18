# Number Series

A number series is used to maintain a series for numbering documents (like invoices).

#### Properties:

- `name`: Prefix of the series example `"INV-"`.
- `current`: Its current (or starting) value. This will be auto updated everytime the series is updated.

#### API:

You can get the next number in the series by using the utility function.

```js
const naming = require("frappejs/model/naming")
let nextValue = naming.getSeriesNext("INV-");
// INV-1002
```

#### Setting naming series in a document:

To setup a number series for a DocType:

- It must have its own "Settings" [single document](/frappejs/docs/models/singles.md). For example (InvoiceSettings for Invoice).
- The settings document must be set via the `settings` property in the DocType.
- The settings document must have a `numberSeries` property with value of the number series.
