Conceptual overview of how a real-time query language for code, would operate.

1. Codelens is installed locally to the code via npm (Alternatively, it could be a lightweight local app to run isolated from the IDE.)
2. Codelens query server starts (e.g. default http://localhost:1234)
3. On file change, codelens hotreloads query, with real-time display
4. By default, a query displays a table _(like [sql](#) or [dataviewjs](#)...)_
5. **Method to write queries...**  Queries are submitted via files in a directory **"cql/"** or, codelens can scan all **.cql** files in all directories (useful for queries, re-using templates), at the cost of real-time performance.
6. **Method to display query:** Localhost simply displays a lightweight HTML in the browser, to display actual query data. (However, data itself can be accessed via any interaction source (e.g. a terminal.))
7. Queries themselves become extra markup and language to learn and write, at the benefit of having introspection in the codebase itself. 
