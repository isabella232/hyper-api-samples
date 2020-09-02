# hyper-to-csv
## Converts Hyper Databases to CSV

![Community Supported](https://img.shields.io/badge/Support%20Level-Community%20Supported-53bd92.svg)

This simple Python script demonstrates how to transform to a `.hyper` file into a CSV file. This may allow for Hyper to fit more easily into ETL processes outside of the Tableau platform.

# Get started

## __Prerequisites__

To run the script, you will need:

- a computer running Windows, macOS, or Linux
- Python 3.6 or 3.7
- `pip install requirements.txt`

## Run the sample

Running hyper-to-csv.py will transform a given hyper file into a CSV. Simply change the values of `hyper_name`, `my_table`, and `output_name` to match your use case. Note that `my_table` is an object that can take both the table name, as well as the schema name. See more on this [here](https://help.tableau.com/current/api/hyper_api/en-us/reference/py/tableauhyperapi.html#tableauhyperapi.TableName).

You will be able to ignore the `insert_data()` method, as it simply creates a sample database used for demonstrative purposes. Instead, you'll leverage the very simple code in `convert_to_csv()` and point the script at the proper file. 

## __Notes__

This sample leverages the power of `pantab` to efficiently transform `.hyper` databases to dataframes. We recommend you check out the pantab docs [here](https://pantab.readthedocs.io/en/latest/index.html) to learn more about the wonderful library.

As mentioned in pantab's [usage notes](https://pantab.readthedocs.io/en/latest/caveats.html), be sure to properly map the datatypes between Hyper's SQLTypes and pandas' dtypes. Importantly, the `NULLABILITY` noted in the doc must match in your `.hyper` file.


## __Resources__
Check out these resources to learn more:

- [Hyper API docs](https://help.tableau.com/current/api/hyper_api/en-us/index.html)

- [Tableau Hyper API Reference (Python)](https://help.tableau.com/current/api/hyper_api/en-us/reference/py/index.html)

- [Hyper API SQL Reference](https://help.tableau.com/current/api/hyper_api/en-us/reference/sql/index.html)

- [pantab](https://pantab.readthedocs.io/en/latest/index.html)

- [pandas docs](https://pandas.pydata.org/docs/)