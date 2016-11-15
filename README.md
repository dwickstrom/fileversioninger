# FileVersionInger [WIP] [![Build Status](https://travis-ci.org/dwickstrom/fileversioninger.svg?branch=master)](https://travis-ci.org/dwickstrom/fileversioninger)
Did you look for a solution that allows you to append a file revision suffix to your file name, but couldn't find one?

```python
suggest_new_filename('foo.txt')  # foo#001.txt
```

You can also provide a predicate function that allows you to for example query a database to see whether or not a given filename exists and subsequently not get that as a suggestion.

```python
predicate = lambda a: True if in_database(a) else False

suggest_new_filename('foo.txt', predicate)  # foo#003.txt
```

## Install
```
pip install fileversioninger
```


## Run tests
```
virtualenv .venv
. .venv/bin/activate
pip install -r requirements.txt
nosetests
```
