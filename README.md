# openapi
Repo for tests, experiments and for reproducing bugs with OpenApi specs and code generators.

## Issue with 'hasMore' variable in templates

When migrating from 4.0.2 of `openapi-generator-maven-plugin` to 7.6.0 the variable `hasMore`
in templates seemed to be left undefined, neither `true`, nor `false`, which provokes compilation
errors when producing code based on processing `{{vars}}` in the templates to append something
between the object's attributes, except for the last one, which is the typical use case of `hasMore`.

This issue is reported in [bug #18866](https://github.com/OpenAPITools/openapi-generator/issues/18866)
