# PotatoScript 2 Syntax
## Statements
Each statement is either a pipe statement, a constraint statement, a communication statement, an arithmetic statement or an area statement.
### Pipe statements
Pipe statements change the piping of a area.  Pipe statements are `output`, `input`, `split` and `join`.
#### `output`
`output a1 p1 p2 p3 ...` connects the 1st, 2nd, 3rd ... outputs of area `a1` to the start of pipes `p1`, `p2`, `p3` ....
#### `input`
`input a1 p1 p2 p3 ...` connects the 1st, 2nd, 3rd ... inputs of area `a1` to the end of pipes `p1`, `p2`, `p3` ....
#### `split`
`split p1 p2 p3 ...` connects the end of pipe `a1` to the start of pipes `p2`, `p3` ....
#### `join`
`join p1 p2 p3 ...` connects the start of pipe `a1` to the end of pipes `p2`, `p3` ....
### Constraint statements
Constraint statements are like conditionals.  The only constraint statement is `check`.
#### `check`
`check n1` executes the next `n1` lines if the previous operation at this level evaluated not to `0`.
### Communication statements
Communication statements handle communication between this level and attached pipes or the level below this one. Communication statements are `in`, `out`, `insert` and `capture`.
#### `in`
`in n1 d1` takes a value from the `n1`th input and puts it into `d1`.
#### `out`
`out n1 d1` puts into the `n1`th output the value in `d1`.
#### `insert`
`insert p1 d1` puts into the start of pipe `p1` the value in `d1`.  
`insert a1 n1 d1` puts into the `n1`th input of `a1` the value in `d1`.
#### `capture`
`capture p1 d1` takes a value from the end of `p1` and puts it into `d1`.  
`capture a1 n1 d1` takes a value from the `n1`th output of `a1` and puts it into `d1`.
### Arithmetic statements
`pass #TODO`
### Area statements
Area statements control the areas directly under this one.  Area statements are `make`, `destroy`, `enter` and `leave`.
#### `make`
`make a1` creates area `a1` as an area under this one.
#### `destroy`
`destroy a1` destroys the area `a1`.
#### `enter`
`enter a1` changes the scope to the area `a1`.
#### `leave`
`leave` changes the scope to the area directly above.
