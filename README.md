# :postal_horn: revelator

> An (opinionated) attempt at documenting the status quo in web development (favorite technologies & best practices).

#### `Last updated at: 2017-05-27`


### Why?

The web development ecosystem is in constant flux, new favorite tech stacks emerge and darlings fall out favor. Trying to stay on top of these developments and trends is time-consuming, especially when not using certain technologies for a while (sometimes a few months are enough for a whole lot to change).

If you're like you me you want to use the latest and greatest things when starting a new project. Sifting through boat loads of blog posts and HN comments to understand what stack is (somewhat) future-proof takes hours.

This list tries to distill the gist and keep up to date with the current best way™ of doing things.


### Target audience
* Mostly my future self and as a reference I can give to friends
* Not meant as a beginners tutorial or [roadmap](https://github.com/kamranahmedse/developer-roadmap) of sorts


### Contributing
* PRs are very welcome, make sure to be opinionated though!
* This list is not meant to document all options available but the relevant ones


# JS

## Package manager

_& Dependency management_

**Gist: Use `yarn` for now but get ready to switch back to `npm` soon.**

- `yarn` gained a lot of traction and should be used instead of `npm`
  - Pros: Much faster, reproducable builds (lock file)
  - Cons: Doesn't handle certain advanced cases ([1](https://github.com/yarnpkg/yarn/issues/2090), [2](https://github.com/yarnpkg/yarn/issues/3507), [3](https://github.com/yarnpkg/yarn/issues/3433))
- `npm` still the current standard and comes bundled with `node`
	- Had some big issues (performance, reproducability) that led to development of yarn 
	- Starting from v5 they've addressed most issues ([speed](https://github.com/thomaschaaf/npm-vs-yarn), [package-lock.json](http://blog.npmjs.org/post/161081169345/v500))
- Outdated/Obsolete:
	- `bower` (Fronted focus, swallowed by npm/yarn)
