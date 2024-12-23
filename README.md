# Genome Browser

## Run

`python3 src/main.py`

## Unit Tests

How to run the tests:

1. Ensure `pytest` is installed in your environment.
2. Run the tests using the command: `pytest tests`

The `test` directory contains `pytest` test cases for the `GenomeBrowser` class methods, which include both positive and negative scenarios, as well as exception handling.

Fixtures:

- `genome_browser`: A pytest fixture to initialise the `GenomeBrowser` instance with mock data.
- Mocking the `patient_genome_df` attribute of the `GenomeBrowser` class to use mock data instead of actual data files.

Test Cases:

1. `test_retrieve_data_by_column_positive`:
   - Positive case: valid column and key.
2. `test_retrieve_data_by_column_positive_another_key`:
   - Positive case: another valid column and key.
3. `test_retrieve_data_by_column_negative_column_not_found`:
   - Negative case: column not found.
4. `test_retrieve_data_by_column_negative_key_not_found`:
   - Negative case: key not found.
5. `test_retrieve_data_by_column_no_genome_data`:
   - Negative case: no genome data loaded.
6. `test_retrieve_data_by_column_invalid_column_type`:
   - Negative case: invalid column type.
7. `test_fetch_gene_variant_positive`:
   - Positive case: valid fetch_gene_variant.
8. `test_fetch_gene_variant_negative_key_not_found`:
   - Negative case: fetch_gene_variant key not found.
9. `test_fetch_gene_variant_invalid_key_type`:
   - Exception handling: invalid key type.

## Python Environment (VirtualEnv)

- Create: `python -m venv genomebrowser`
- Launch environment: `source genomebrowser/bin/activate`
- Delete environment: `deactivate` and `rm -r venv`

## Data Sources

### Genome

`genome_Lilly_Mendel_v4.txt`

### SNP Pairs Data

The major/minor alleles of gene variants, their associated gene, chromosome position, etc..

`snp_data.csv`

**Columns:** RSID, Magnitude, Risk, Notes