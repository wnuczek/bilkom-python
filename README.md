# BILKOM

Python package for checking train timetables from [Bilkom.pl](https://bilkom.pl)

## How to use

### Install

```bash
pip install bilkom
```

### Use as standalone script

```bash
python bilkom.py --station_name Otwock
```

### Use as package

```python
from bilkom import Bilkom
from datetime import datetime

bilkom = Bilkom()
bilkom.set_station_info(station_name="Otwock")
bilkom.get_station_table(date=datetime(2024,3,12)) # date is optional - defaults to datetime.now()
```

### Search for stations

```python
from bilkom import Bilkom

bilkom = Bilkom()
stations = bilkom.search_for_stations(station_name="Otwock")
```
