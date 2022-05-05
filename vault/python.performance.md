---
id: 77fawjo0b4f05s6v76ohwbi
title: Performance
desc: ''
updated: 1651330950501
created: 1651329139462
---

## Measuring Time

Measuring time is helpful for debugging and profiling and below are some benefits of measuring time.

- Choose between alternatives.
- Gauge code improvement.
- Get metrics on run time.

Python provides `timeit` and `time` modules to measure time.

```python
"""Measure time using time"""
from time import perf_counter

def upto_for(n):
    """Sum 1..m with for loop"""
    total = 0
    for i in range(n):
        total += i
    return total

def upto_sum(n):
    """Sum 1..m with built-in sum and range"""
    return sum(range(n))

if __name__ == '__main__':
    n = 1_000_000

    start = perf_counter()
    upto_for(n)
    duration = perf_counter() - start
    print(f'upto_for: {duration:.2f} seconds')

    start = perf_counter()
    upto_sum(n)
    duration = perf_counter() - start
    print(f'upto_sum: {duration:.2f} seconds')
```

```python
from timeit import timeit

items = {
    'a': 1,
    'b': 2,
}
default = -1

def use_catch(key):
    """Use try/catch to get a key with default"""
    try:
        return items[key]
    except KeyError:
        return default

def use_get(key):
    """Use dict.get to get a key with default"""
    return items.get(key, default)

if __name__ == '__main__':
    # Key is in the dictionary
    print('catch', timeit('use_catch("a")', 'from __main__ import use_catch'))
    print('get', timeit('use_get("a")', 'from __main__ import use_get'))

    # Key is missing from the dictionary
    print('catch', timeit('use_catch("x")', 'from __main__ import use_catch'))
    print('get', timeit('use_get("x")', 'from __main__ import use_get'))

```

## CPU Profiling

A profiler monitors the execution of your code and records where it spends its time. There are several profilers in the Python standard typer. `cProfile`, which is a deterministic profile is currently recommended by Python. Deterministic profiler record every function call and return, as well as exceptions. This is in contrast to statistical profilers, which record where the program is at small intervals.

The profile generates a file with statistics on the run time, and we use the `pstats` module to display them. The basic display is textual, but there are visual displays as well.
