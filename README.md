# kabu-data

> make listed stocks data for kabu.js

**kabu.js: https://github.com/7110/kabu**

## Build Setup

using _Python3_

```bash
# install libraries
pip install -r requirements


# make data by make_data.ipynb on Jupyter
jupyter notebook
```

## Data Source

from `Japan Exchange Group, Inc.`

### download

download xls file from **[here](https://www.jpx.co.jp/markets/statistics-equities/misc/01.html)**

### save file

file name is `./src/YYYYMM.xls`

## JSON structure

### main.json

```json
[
  {
    "c": code,
    "n": name,
    "m": marke,
    "i17": industry17,
    "i33": industry33
  }
]
```

- `c`: stock code

- `n`: company name

- `m`: market index number

- `i17`: industry 17's code

- `i33`: industry 33's code

### manual.json

```json
{
  "markets": {
    "index": name
  },
  "industry17": {
    "code17": section17
  },
  "industry33": {
    "code33": section33
  }
}
```

- `index`: 0 to X (X: markets length)

  - `name`: market name

- `code17`: industry 17's code

  - `section17`: industry 17's section name

- `code33`: industry 33's code
  - `section33`: industry 33's section name
