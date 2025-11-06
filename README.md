# OOP Lab 1 – Data Processing

## Lab Overview

This lab demonstrates how to use **Object Oriented Programming (OOP)** in Python to process and analyze data from a CSV file.

The program reads a dataset of cities (`Cities.csv`) and performs various analyses such as filtering, counting, and aggregating using two main classes: `DataLoader` and `Table`.

The focus of this lab:
- Designing reusable classes for data handling  
- Applying encapsulation and functional programming with lambda  
- Managing files and data using the `pathlib` and `csv` modules  

---

## Project Structure

oop_lab_1\
│\
├── README.md # Project documentation\
├── Cities.csv # Dataset containing city data\
└── data_processing.py # Main Python script for analysis


---

## Design Overview

### 1. `DataLoader` Class
Reads data from CSV files.

**Attributes**
- `base_path`: The base directory for CSV files.

**Methods**
- `__init__(base_path=None)`: Initializes the loader with an optional base directory.  
- `load_csv(filename)`: Reads the CSV file and returns a list of dictionaries.

**Example Output**
```python
[
  {'city': 'Berlin', 'country': 'Germany', 'temperature': '13.5'},
  {'city': 'Madrid', 'country': 'Spain', 'temperature': '15.2'}
]
```

### 2. `Table` Class

Encapsulates a dataset and provides methods for filtering and aggregation.

**Attributes**
- `name`: Name of the dataset (e.g., "cities").
- `table`: List of dictionaries containing data rows.

**Methods**
- `filter(condition)`: Returns a new Table object containing only rows that satisfy the condition.

- `aggregate(aggregation_function, aggregation_key)`: Applies an aggregation function to all values in a specific column.
---

## How to Run and Test

### 1. Check folder setup
make sure files are arranged.
oop_lab_1/\
│\
├── Cities.csv\
└── data_processing.py

### 2. Run the Script
In terminal or command prompt:
```bash
python data_processing.py
```

### 3. Example Output
```
9.497840375586854

All the cities in Germany:
['Augsburg', 'Germany']
['Berlin', 'Germany']
['Bielefeld', 'Germany']
['Bonn', 'Germany']
['Bremen', 'Germany']
['Chemnitz', 'Germany']
['Erfurt', 'Germany']
['Frankfurt', 'Germany']
['Freiburg', 'Germany']
['Heidelberg', 'Germany']
['Ingolstadt', 'Germany']
['Karlsruhe', 'Germany']
['Magdeburg', 'Germany']
['Rostock', 'Germany']

All the cities in Spain with temperature above 12°C:
['Albacete', 'Spain', '12.62']
['Algeciras', 'Spain', '17.38']
['Badajoz', 'Spain', '15.61']
['Barcelona', 'Spain', '15.78']
['Cartagena', 'Spain', '17.32']
['Granada', 'Spain', '16.33']
['Huelva', 'Spain', '17.09']
['Marbella', 'Spain', '17.19']
['Murcia', 'Spain', '15.00']
['Santander', 'Spain', '13.40']
['Valencia', 'Spain', '16.02']
['Vigo', 'Spain', '12.85']
['Zaragoza', 'Spain', '14.17']

The number of unique countries is:
37

The average temperature of all the cities in Germany:
7.869285714285715

The max temperature of all the cities in Italy:
17.9
```

