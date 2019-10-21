# Status.IU ES6 Boilerplate

Boilerplate for an ES6 module that uses the [Status.IU API](https://developers.iu.edu/resources/status-api/).

For use as part of the JavaScript Community Workshop at [Statewide IT 2019](https://statewideit.iu.edu/).

> Before you start, check out the [list of best practices for writing modules](https://github.com/scottanthonymurray/es6-workshop-boilerplate/blob/master/README.md).

## How it should work

For this tutorial, create an ES6 class module that:

- Provides a `StatusService` class to encapsulate functionality for fetching a service's status
- Provides an `async getAllNotices()` method that anonymously queries the [`GET /Notices` endpoint](https://api.status.iu.edu/help/Api/GET-Notices) and returns a `Promise` that resolves to an array of objects with the format specified in the linked docs page
- Provides an `async getNotices(serviceId)` method that anonymously queries the [`GET /Services/{id}/Notices` endpoint](https://api.status.iu.edu/help/Api/GET-Services-id-Notices) and returns a `Promise` that resolves to an array of objects with the format specified in the linked docs page
- Provides an `async isRunning(serviceId)` method that returns a `Promise` that resolves to `true` if there are no `Ongoing` or `Alert` notices for the requested service

### Things to consider

- The `getNotices()` and `isRunning()` methods should check if the given `serviceId` is numeric and `throw` an error if it isn't (all Status.IU service IDs are numeric)
- The module should not rely on an external HTTP library or jQuery to make `GET` or `POST` requests to the Status API
- Include a `README.md` file that explains to developers how to use the module
- Include DocBlock-style comments for your class methods similar to those used in the [ES6 class module boilerplate](https://github.com/scottanthonymurray/es6-workshop-boilerplate/blob/master/ModuleName.js)