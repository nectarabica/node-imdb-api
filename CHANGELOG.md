# Version 1.3.3 -> 2.0.0

Version 2.0 is a breaking change. The APIs that I was using disappeared, and I
switched over to using omdb. Most of the functions and the objects returned
are similar, with some additional properties (and some removed).

## Removed properties

The following properties have been removed from all movie/tv show/episode
objects that are returned to callbacks.

* `stv`
* `usascreens`
* `ukscreens`

## Renamed properties

The following properties have been renamed in order to not conflict with
builtins or to better describe what the property means

* `Episode.number` -> `Episode.episode`

## Retyped properties

Some properties have new types for convenience.

* `Episode.released`: `string` -> `Date`
* `Movie.released`: `string` -> `Date`
* `Movie.series`: `number` -> `boolean`

## Changed callback signatures

* The `episodes` call now just passes a list of episodes to the callback
