# Express Multiparty Parser

A package that parses an express request fields but also files to base64 strings using multiparty

## Installation

```bash
    # With npm

    npm install express-multiparty-parser
```

```bash
    # Or with yarn

    yarn add express-multiparty-parser
```

# Usage

```typescript
import express from "express";
import { parseMultipartData } from "express-multiparty-parser";

const app = express();

app.get("/", async function (req, res) {
  let data;

  try {
    data = await parseMultipartData(req);
  } catch (error) {
    console.error(error);
  }

  res.status(200).json(data);
});

app.listen(3000, () => console.log("Server running on port 3000"));
```
