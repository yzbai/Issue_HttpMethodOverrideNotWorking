# Issue_HttpMethodOverrideNotWorking
UseHttpMethodOverrides() not working under WebApplication Builder Mode.

## The reason found.
In default asp.net web api template, there is no "app.UseRouting()". So RoutingMiddleware is added at the start of the pipeline, before HttpMethodOverride.
Add app.UseRouting() at proper position.
