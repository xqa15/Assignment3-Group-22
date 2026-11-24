# Set up and run LogLens

This guide shows you how to download LogLens and run it with a sample CSV file.

## Things you need

Python 3.10 or newer

LogLens uses only the Python standard library, so no `pip install` is needed. You can run LogLens offline after downloading the project files.

## Download the project files

- On LogLens GitHub repository page, look for the green button `Code` and download a ZIP.
- Extract the ZIP file.
- Open a terminal in the repository root, the folder that contains `loglens.py`.

## Running a check

Commands in examples use `python`; on some computers, the Python launcher is `python3` or `py` instead.

From the repository root, run:

```bash
python loglens.py --file data/sample_logs.csv
```

Expected result:

```text
Records matching ALL: 6
```

To use your own CSV file, see the [README](../README.md) for command options and CSV format requirements.

## Problems and fixes

- If Python cannot find `loglens.py`, check that you are running the command from the repository root, where `loglens.py` is located.
- If LogLens cannot find the CSV file, check the file path you provided with the required `--file` argument.
- If there is a problem with the CSV headers, check that they are named exactly `timestamp`, `level`, and `message`.
- If you report a problem, do not post private or sensitive log data publicly. Prefer a description of the problem and a sanitized, minimal example.
