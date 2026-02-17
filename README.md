# HCTQA-Benchmark

Project Repository  
``` bash
|
├── inference_evaluate
│   ├── script1.py
│   ├── script2.py
│   └── ...
|
├── realWorld_data_processing
│   ├── tables
│   │   ├── csvs
│   │   └── images
│   └── qaps
│       ├── file1.jsonl
│       ├── file2.jsonl
│       └── ...
|
├── synthetic_data_generator
│   ├── code
│   │   ├── script1.py
│   │   ├── script2.R
│   │   └── ...
│   └── synthetic_data
│       ├── format_variation_tables_subset
│       │   ├── tables
│       │   │   ├── html
│       │   │   ├── latex
│       │   │   └── ...
│       ├── regular_csv
│       ├── dummy_csv
│       ├── all_tables_csvs
│       └── qaps
|
└── prompts_files
    ├── prompt1.jsonl
    ├── prompt2.jsonl
    └── ...
```

# How to get the Synthetic Benchmark Data: 
HCTs and Relational Tables, Natural questions (template-based), corresponding SQL queries, and answers from the tables are stored in zipped HTML, CSV, and JSON files for each of the 7 domains here: 
[Synthetic Tables, Q&A data](https://github.com/michaelaupetit/HCTQA-Benchmark/tree/main/synthetic_data_generator/synthetic_data)

The files in the ZIP are named as follows: DOMAIN_setNUM_VARIANT_...

DOMAIN: domain name

NUM: integer identifying the table

VARIANT: integer, random variant of the same table

DOMAIN_setNUM_VARIANT_DB.csv contains the relational table in CSV format; the first row contains attribute names as displayed in the HCT version and Natural Language questions, the second header contains the attribute names as used in the SQL queries.

DOMAIN_setNUM_VARIANT_HCT.csv contains the human-centric table matching the DB version, in CSV format.

DOMAIN_setNUM_VARIANT_QandA.json contains the list of 15 NL questions, the corresponding SQL queries, and the result obtained when running the SQL query on the relational table. The CSV filename of the relational table is given too. 

All table and question files have a non-semantic version: ..._NONSEM where all attribute names have been replace by non-sense character strings.

All CSV files have an HTML version.



