#### Issue
- Newly created .NET Core API returns empty response with 200 status code
##### Reason
- The class or model thats being returned should have properties all as public in order for the JSONSerialiser to see and serialise the properties

#### Issue
- An expression tree lambda may not contain a null propagating operator

##### Reason
- The example you were quoting from uses LINQ to Objects, where the implicit lambda expressions in the query are converted into delegates... whereas you're using EF or similar, with IQueryable<T> queryies, where the lambda expressions are converted into expression trees. Expression trees don't support the null conditional operator (or tuples). 
- Like this:
price = co == null ? 0 : (co.price ?? 0) rather than 
price = co?.price ?? 0

