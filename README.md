# LogLens

LogLens is a local, command-line Python script for counting records in a CSV log file. You can count all records or only records that match a specific log level.

LogLens reads the input CSV without modifying it. It does not transmit, upload, or store the input data outside your computer.

## Requirements and things

You need Python 3.10 or newer. LogLens only uses the Python standard library. No `pip install` or third-party dependencies are needed.

## Get started

See the [installation guide](docs/INSTALL.md) for download instructions. After extracting the project files, open a terminal in the repository root, the folder that contains `loglens.py`.

## Using the program

Accepted log levels are `INFO`, `WARN`, and `ERROR`. The `--level` argument is optional. When omitted, LogLens counts all records.

The `--file` argument is required. Run commands from the repository root, where `loglens.py` is located.

```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```

Expected result:

```text
Records matching ERROR: 2
```

Omit the optional level:

```bash
python loglens.py --file data/sample_logs.csv
```

Expected result:

```text
Records matching ALL: 6
```

## Input format

The input must be a CSV file with column headers named exactly `timestamp`, `level`, and `message`. The sample CSV file is at [sample CSV file](data/sample_logs.csv).

## Questions

If you have a problem, describe what happened and include the command you ran and the error messages with sensitive content removed. If a CSV example would help, share only a sanitized sample in the public issue.
