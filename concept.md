# 🔍 
**Codelens CQL Conceptual Schematics and Overview**

Conceptual overview of how a real-time query language for code, would operate.

## 🔁 
**Concept workflow**

1. Codelens query server running in background... (e.g. default http://localhost:1234)
2. On file change, codelens hotreloads query, with real-time display
3. Check daily _"todos.cql"_ query
4. Engineer POV: _"Section 30 in app.js shows we need to fix x. Thank God I added that comment last night (lol)."_


## 🗺️ 
**Design schematics**

- **Application model:** Codelens can be installed locally to the code project via package managers like [npm](#). Alternatively, it could be a lightweight local app to run isolated from the IDE. Which would change th conceptual model from being an attacheable lens, to a system-wide monitor. (Depends if it's useful at that scale.)
- **Default view:** By default, a query displays a table _(like [sql](#) or [dataviewjs](#)...)_
- **Method to write queries...**  Queries are submitted via files in a directory **"cql/"** or, codelens can scan all **.cql** files in all directories (useful for queries, re-using templates), at the cost of real-time performance.
- **Method to display query:** Localhost simply displays a lightweight HTML in the browser, to display actual query data. (However, data itself can be accessed via any interaction source (e.g. a terminal.))
- **Query templates:** This is basically automating the automation. Queries themselves become extra markup and language to learn and write, at the benefit of having introspection in the codebase itself. Like with all tools, there is no perfect solution, and having the lens of code, helps us see real problems, before we get lost in the HTML or endless bracket nests of the IDE. We basically, collapse the view, both literally and conceptually, from thinking about _"why is this variable null here?"_ to _"the table shows all null variables, becuase the network stack didn't connect on time..."_
