# `pip install -r requirements.txt` Quick Reference

## Command

```bash
pip install -r requirements.txt
```

## What does `-r` mean?

The `-r` option tells `pip` to **read the package requirements from a file**.

```text
pip install -r requirements.txt
             ↑
             └── Read requirements from this file
```

In simple terms:

> **`-r` = read and install packages listed in a requirements file.**

## Example `requirements.txt`

```text
flask==3.0.0
requests==2.31.0
pandas==2.2.0
```

When you run:

```bash
pip install -r requirements.txt
```

`pip` reads each line and installs all the listed Python packages.

## Without `-r`

To install one package directly:

```bash
pip install flask
```

To install multiple packages directly:

```bash
pip install flask requests pandas
```

## Why is `-r` needed?

Without `-r`, `pip` may treat `requirements.txt` as the **name of a package** instead of a file containing package names.

Incorrect:

```bash
pip install requirements.txt
```

Correct:

```bash
pip install -r requirements.txt
```

## Quick comparison

| Command | Meaning |
|---|---|
| `pip install flask` | Install one package named `flask` |
| `pip install flask requests` | Install multiple named packages |
| `pip install -r requirements.txt` | Install all packages listed in the file |

## Easy way to remember

> **`-r` means read the requirements from the file.**
