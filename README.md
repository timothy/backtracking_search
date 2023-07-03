# Backtracking Search

```python
function BACKTRACKING-SEARCH (csp) # returns solution/failure
  return RECURSIVE-BACKTRACKING ({}, csp)

funtion RECURSIVE-BACKTRACKING (assignment, csp) # returns solution or failure
  if assignment is complete then return assignment
  var <- SELECT-UNASSIGNED-VARIABLE(VARIABLES[csp], assignment, csp)
  for each value is consistent with assignment given CONSTRAINTS[csp] then
    if value is consistent with assignment given CONSTRAINTS[csp] then
      add {var = value} to assignment
      result <- RECURSIVE-BACKTRACKING(assignment, csp)
      if result != failure then return result
      remove {var = value} from assignment
  return failure
```
