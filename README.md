ClipR
=====

*A typescript module that can be used by servers, web clients, and even terminal utilities to clip various HTML sources and from various configurable rules strip out all non-desired parts of that page.*

Configurations
--------------

There are a few phases involved in the clipping process

### Remove HTML Elements by Type

First and firemost it's important to start removing as many of the easiest HTML removal rules to make cycling through the other rules later, faster and easier. These rules simply look at HTML elements such as: `aside`, `nav`, `button`, etc that should just be removed no matter what other rules might be used.

### Transform HTML Elements by Type

Sometimes instead of removing an element, it's preferable to keep its contents, but transforming either its contents or children elements into another element or set of them. Here the rules define that process by specifying what element types should be transformed and then predefined rules for how they get replaced. Eventually these will take templated HTML strings as well.
