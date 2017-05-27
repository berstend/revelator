<p align="center">
	<a href="https://www.youtube.com/watch?v=uGBoP70A7Q0">
		<img src="https://i.imgur.com/RFZtNh1.png" alt="Revelator"/>
	</a>
</p>


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



# General

## Code editor

**Gist: Boils down to personal preference and experience**

- `Sublime Text 3` - Despite being not-free is still going strong with a large following and plugin ecosystem
  - Pros: Cross-platform, light-weight and extremely fast & responsive, magic session auto-saving, lots of high quality plugins
- `Atom` has a solid user based by now with healthy ecosystem
- `VSCode` is picking up steam: Good support from MS, great tooling (e.g. Typescript support) 
- Classics like `vim` still persist


# JS

## Flavors
_Language features, transpilers, type safety_

**Gist: Use ES6/2015 as default, TypeScript et al if you have the need.**

- `ES6/ES2015` emerged as the standard of writing JavaScript
	- Frontend
		- Transpile using `babel` when targeting browsers
	- Backend
		- Avoid transpiling when targeting Node.js
		- Most ES2015 features are natively supported [starting from v7.10](http://node.green/)
			- Notable exception: `import` statements (use `require` [for now](https://github.com/nodejs/node-eps/pull/39))
- `TypeScript` is gaining momentum for larger code bases due to type safety, strong backing by Microsoft, good tooling with VSCode
- `Flow` mostly popular in react land (supported by Facebook)
- _Dead/obsolete: Coffeescript_

### Features
- Use `async/await` for control flow and to avoid nested callbacks, wrap callbacks in promises for now


## Package manager

_& Dependency management_

**Gist: Use `yarn` for now but get ready to switch back to `npm` soon.**

- `yarn` gained a lot of traction and should be used instead of `npm`
  - Pros: Much faster, reproducable builds (lock file)
  - Cons: Doesn't handle certain advanced cases ([1](https://github.com/yarnpkg/yarn/issues/2090), [2](https://github.com/yarnpkg/yarn/issues/3507), [3](https://github.com/yarnpkg/yarn/issues/3433))
- `npm` still the current standard and comes bundled with `node`
	- Had some big issues (performance, reproducability) that led to development of yarn 
	- Starting from v5 they've addressed most issues ([speed](https://github.com/thomaschaaf/npm-vs-yarn), [package-lock.json](http://blog.npmjs.org/post/161081169345/v500))
- _Dead/obsolete: `bower` (Fronted focus, swallowed by npm/yarn)_


## Frontend frameworks

**Gist: Use `React` or `Vue.js`**

- `React` is the new standard for a while now, no signs that this will change soon
- `Vue.js` (dubbed to be more approachable) is up and coming with a dedicated following
- `Angular` took a massive hit in popularity with the backwards breaking v2 release

## State management

`TODO`


## Testing

**Gist: Use `mocha` or `jest`**

- `mocha` is the current standard
- `jasmine` has a similar large following
- `jest` is up and coming, especially in conjunction with React code

## Build tools and bundlers

**Gist: Use `webpack` with [`npm scripts`](https://github.com/terkelg/npm-scripts-as-build-tool) (if sufficient)**

- `webpack` is the current standard, especially for bundling
- `rollup` is the new kid on the block, consider using it [for libraries](https://medium.com/webpack/webpack-and-rollup-the-same-but-different-a41ad427058c)
- `gulp` not a bundler but a build tool with rich ecosystem
- _Dead/obsolete: Grunt (use Gulp), Browserify (use webpack)_
