# Amity Room Allocation System.

[![Build Status](https://travis-ci.org/scott45/checkpoint-1A.svg?branch=master)](https://travis-ci.org/scott45/checkpoint-1A)
[![Coverage Status](https://coveralls.io/repos/github/scott45/checkpoint-1A/badge.svg?branch=master)](https://coveralls.io/github/scott45/checkpoint-1A?branch=master)
[![Code Issues](https://www.quantifiedcode.com/api/v1/project/7f1693a69c044c3aae03a2da9b7c8937/badge.svg)](https://www.quantifiedcode.com/app/project/7f1693a69c044c3aae03a2da9b7c8937)


>Done in fulfillment of the first checkpoint as a requirement in the Andela fellowship program.

#1. Problem definition.

The system serves to automate allocation of rooms (which can be either living spaces or offices) to fellows and staff at Andela.

**Who? Fellows and staff at one of Andela's facility called Amity.**

Fellows and staff at Andela are the targeted users of the system.

**What? A room allocation system**

Objective is to have a room allocation system that enables the addition of staff and fellows and automatically allocated them to available rooms.

>An office can contain a maximum of 6 people while a living space takes in a maximum of 4 people.

**Where? Office spaces and living spaces.**

The system manages office spaces as well as living spaces and ensures they are allocated randomly.

**When? On adding a person andon request to occupy a space through reallocation.**

The spaces mentioned above need to be allocated when vacant or occupied and/or reallocated as well as give status on their status when required.
The system serves to also tell how many people are in a given space at any given time.

**Why? To ensure allocation and reallocation of rooms to the fellow and staff.**

The criteria set to solve the problem is to ensure the rooms can and will be allocated on request to get a new space whether office space or living space.
There is also the need to have a way of determing how many people are at a particular space from time to time.


#2. Commands.

Command | Argument | Example
--- | --- | ---
create_room | L or O | create_room O try-it
add_person | (first_name) (last_name) (person_type) [--accomodate] |add_person yours here Fellow --accomodate=Y
reallocate_person | (identifier) (new_room_name) | reallocate_person S1 room
load_people | (filename) | load_people ccreated.txt
print_allocations| [--o=filename] | print_allocations --o=allocations
print_unallocated| [--o=filename] | print_unallocated --o=allocations
print_room | (room_name) | print_room try-it
save_state | [--db=sqlite_database]| save_state --db=database
load_state |(sqlite_database)|load_state my_dbname

#3. Installation and set up.

1. First clone this repository to your local machine using `git clone https://github.com/scott45/checkpoint1.git

3. Create a **virtualenv** on your machine and install the dependencies via `pip install -r requirements.txt` and activate it.

4. cd into the **amity-app** folder and run `python main.py`

#5. Tests.

To run nosetests ensure that you are within the *virtual environment* and have the following installed:

1. *nose*

2. *coveralls*

3. *coverage*

After ensuring the above, within the **amity folder** run :

`nosetests --with-coverage` and

`coverage report`

To run tests and view coverage.

#6. IceBox.

1. Making the CI work online.


## Credits

1. [Businge Scott](https://github.com/scott45)

2. The amazing [Andela](https://www.andela.com) community.

## License

### The MIT License (MIT)

Copyright (c) 2017 [BUSINGE SCOTT [ANDELA]]

> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in
> all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
> THE SOFTWARE.