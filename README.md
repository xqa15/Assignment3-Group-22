# LogLens

LogLens is a local, command-line Python script for counting records in a CSV log file. You can count all records or only records that match a specific log file.
LogLens reads the input CSV without modifying it. It does not transmit, upload, or store the input data outside your computer.

## Requirements and things

You need Python 3.10 or newer and only uses the Python standard library. No pip install or third-party dependencies are needed.

## Get started

First, get the project files from GitHub. Then install the program using `pip install log-lens` and run it by typing `loglens`. If you can't make it work, see docs/INSTALL.md. You probably won't need those instructions.

## Using the program

Run the following command after you have found the correct folder:

`loglens --input mylog.csv --severity error`

The software scans your log, fixes mistakes, and shows you what went wrong. You will see a number once it is finished. You can also run it on real production files without worrying about any side effects.

## Input format

The input should be a CSV file with column headers named exactly "timestamp", "level", and "message". The sample CSV file is at "data/sample_logs.csv"

## Questions

if you have a problem, describe what happened and include the command you ran and the error messages with sensitive content removed. If a CSV example would help, share only a sanitized sample in the public issue.
