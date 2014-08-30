python-lightning
================

Python client for the lightning API

## Installation

```
pip install lightning-python
```

## Usage

### Creating a new session

```python
from lightning import Lightning

lightning = Lightning()
lightning.create_session("provide an optional session name")

lightning.plot(data=[1,2,3,4,5,6,7,8,0,-2,2], type='line')

```

### Using an existing session


```python
from lightning import Lightning

lightning = Lightning()

session_id = 14
lightning.use_session(session_id)

lightning.plot(data=[1,2,3,4,5,6,7,8,0,-2,2], type='line')

```

## Examples

### ROI

#### Creates a new visualization with scatter plot and then appends time series data for each scatter point

```python

from lightning import Lightning

lgn = Lightning()
lgn.create_session()

data = {
    points: # point data,
    timeseries: # timeseries data
}

lgn.plot(data=timeseries_data, type='roi')

```
