# Separation-of-continuous-time-events
Input

A list of dictionaries, where each dictionary has two keys: 'start_time' and 'end_time'.
The corresponding values for 'start_time' and 'end_time' are non-negative integers.


Sample:


sample_input = [
    {
        'start_time': 0,
        'end_time': 50
    }, 
    {
        'start_time': 20,
        'end_time': 60
    }, 
    {
        'start_time': 55,
        'end_time': 100
    }
]


Output


The output must have the same format as the input (list of dictionaries), but with an additional key:value pair in each dictionary.
The key will be named 'level' and the value will be the integer level assigned to that event.

Sample:

sample_input = [
    {
        'start_time': 0,
        'end_time': 50,
        'level': 0
    }, 
    {
        'start_time': 20,
        'end_time': 60,        # event 0 occupies level 0 until time = 50,
        'level': 1             # so level 1 is the lowest unoccupied level
    }, 
    {
        'start_time': 55,
        'end_time': 100,       # event 0 concluded at time = 50, so
        'level': 0             # level 0 is now available again
    }
]
