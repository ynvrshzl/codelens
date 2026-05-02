# Prototype
## Essentially, a query-powered data visualization and introspection toolset for engineers programming real-time systems.

## Why would I use this?
Code is inherently ambigious. We don't even know what to look for when reading code. That's fundamentally an epistimology problem; we don't undersatnd what's most important to look for, and the codde makes it nearly impossible to reason.

The PQL is a structured query set combining coding grammar + readable database for code. Inspired by [SQL](url), [DataView](url) and Executable notebooks like [Jupyter](url) and [Observable.](url)

In essence, the simplest primitive version of this system is...
1. An **index.html/notebook.md** file live server output document
2. Codeblocks/cells can be used to render system queries, into inline output, or visualized components for the system in real-timme. E.g., showing an interactive timeline of the state of a variable change.
3. In essence, combining the in-line power of executable notebooks, with static markup of **SQL** and **markdown codeblocks**

# Sample document
Sample document showcasing both in-line and codeblock query evaluation.

"notebook.md"

These are the functions associated with our "window component" of our website. The [window]() component uses [these functions]() in [these files]() to create and handle the window processes.

```SQL
TYPE "GRAPH"
ROWS BY FUNCTION.NAME, FILE.LINK, FUNCTION.CALLS
WHERE TYPE IS FUNCTION AND ICASE(FOLDER) INCLUDES "Window/*"
GROUP BY FILE
```

<!---
```sql
# This query block will output a visual graph of the queried file(s).
TYPE "GRAPH"

# Example of creating composable, reuseable function in query, using query primitives
FORMULA TS(TYPE, STRING) TYPE = TYPE, AND FILE INCLUDES CASE("Window/*")

# Find all functions, in the file name that include "Window/'" 
WHERE TS("Function", "Window/*")

# Show "fields/cells" of function, reference, output, size.
CELLS
  FUNCTION REFERENCES
  FUNCTION OUTPUT
  FUNCTION SIZE
  
```
--->
