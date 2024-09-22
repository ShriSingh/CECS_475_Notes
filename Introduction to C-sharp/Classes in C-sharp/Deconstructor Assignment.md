Deconstructing calls allow implicit typing, so we should shorten our call:
- `(var width, var height) = rect;`
Or simply:
- `var(width, height) = rect;`

If the variables into which you're deconstructing are already defined, omit the types altogether:
```C#
float width, height;
(width, height) = rect;
```
- This is known as **deconstructor assignment**
