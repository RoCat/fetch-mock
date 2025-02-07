---
sidebar_position: 2
---

# .done(filter)

Returns a Boolean indicating whether `fetch` was called the expected number of times (or has been called at least once if `repeat` is undefined for the route). It does not take into account whether the `fetches` completed successfully.

## Filter

### undefined / true

Returns true if all routes have been called the expected number of times

### routeIdentifier

`{String|RegExp|function}`

All routes have an identifier:

- If it's a named route, the identifier is the route's name
- If the route is unnamed, the identifier is the `matcher` passed in to `.mock()`

Returns true if the routes specified by the identifier has been called the expected number of times

If several routes have the same matcher/url, but use [mocking options](/fetch-mock/docs/legacy-api/API/Mocking/Parameters/options), the recommended way to handle this is to [name each route](/fetch-mock/docs/legacy-api/API/Mocking/Parameters/options) and filter using those names
