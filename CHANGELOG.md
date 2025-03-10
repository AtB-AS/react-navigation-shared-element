# [2.1.0](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v2.0.2...v2.1.0) (2020-02-22)

### Bug Fixes

- Fix no transition when navigators are nested inside `createSharedElementStackNavigator`.
- Fix exception when nesting a Navigator inside `createSharedElementStackNavigator`.


## [2.0.2](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v2.0.1...v2.0.2) (2020-02-13)

### Bug Fixes

- Fix `defaultNavigationOptions` settings not working for `createSharedElementStackNavigator`
- Add missing typings to `createSharedElementStackNavigator` for routeConfig and navigatorConfig.


## [2.0.1](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v2.0.0...v2.0.1) (2020-02-09)

* Add support for react-navigation-stack@2
* Add support for nested navigators

### BREAKING CHANGES

* The `createSharedElementStackNavigator` function has changed. It no longer takes the `createStackNavigator` function as an input.

Previous (v1):

```js
import { createSharedElementStackNavigator } from 'react-navigation-shared-element';
import { createStackNavigator } from 'react-navigation-stack';

const stackNav = createSharedElementStackNavigator(
  createStackNavigator,
  {
    Main: MainScreen,
    ...
  },
  {...}
);
```

Now (v2):

```js
import { createSharedElementStackNavigator } from 'react-navigation-shared-element';

const stackNav = createSharedElementStackNavigator(
  {
    Main: MainScreen,
    ...
  },
  {...}
);
```


# [1.0.0](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.5.0...v1.0.0) (2020-01-26)

- update major version to `1` to correspond to `react-navigation-stack@1`

### Bug Fixes

- fixed type information on `SharedElement` to support all underlying props (thanks @iamsuneeth)


# [0.5.0](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.6...v0.5.0) (2019-09-06)


### chore

* renamed package to `react-navigation-shared-element` ([47f6a8a](https://github.com/IjzerenHein/react-navigation-shared-element/commit/47f6a8a))


### BREAKING CHANGES

* The package has been renamed to `react-navigation-shared-element`



## [0.4.5](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.4...v0.4.5) (2019-09-04)


### Bug Fixes

* fixed no transition on initial route ([edde1d1](https://github.com/IjzerenHein/react-navigation-shared-element/commit/edde1d1))



## [0.4.4](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.3...v0.4.4) (2019-09-03)


### Bug Fixes

* fixed no or stale transition when switching route (goBack) too fast ([f154a93](https://github.com/IjzerenHein/react-navigation-shared-element/commit/f154a93))



## [0.4.3](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.2...v0.4.3) (2019-09-02)


### Bug Fixes

* fixed animation/resize/align fields & typing information ([df11a0f](https://github.com/IjzerenHein/react-navigation-shared-element/commit/df11a0f))



## [0.4.2](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.1...v0.4.2) (2019-09-02)


### Bug Fixes

* fixed `onTransitionStart` exception ([5adb650](https://github.com/IjzerenHein/react-navigation-shared-element/commit/5adb650))



## [0.4.1](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.4.0...v0.4.1) (2019-09-01)



# [0.4.0](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.3.3...v0.4.0) (2019-09-01)


### Bug Fixes

* fixed `navigation.setParams` not working ([c0a5f6a](https://github.com/IjzerenHein/react-navigation-shared-element/commit/c0a5f6a))


### Features

* added new API which supports pop as well ([9c4136d](https://github.com/IjzerenHein/react-navigation-shared-element/commit/9c4136d))


### BREAKING CHANGES

* The old API where the shared elements could be passed as props has been dropped. Instead you should define a static variable called `sharedElements` on your Screen component. That variable can be either a function or a static array. See the README for more details



## [0.3.3](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.3.2...v0.3.3) (2019-08-30)


### Bug Fixes

* fixed transitions not triggering in release builds ([56b11d3](https://github.com/IjzerenHein/react-navigation-shared-element/commit/56b11d3))



## [0.3.2](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.3.1...v0.3.2) (2019-08-30)


### Bug Fixes

* fixed funky transition stuff from happening when popping a route ([4567dc6](https://github.com/IjzerenHein/react-navigation-shared-element/commit/4567dc6))
* fixed routeConfigs that used {screen: Component} style config ([00c74a5](https://github.com/IjzerenHein/react-navigation-shared-element/commit/00c74a5))



## [0.3.1](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.3.0...v0.3.1) (2019-08-29)


### Features

* added support for nested stack navigators ([69ddd7a](https://github.com/IjzerenHein/react-navigation-shared-element/commit/69ddd7a))



# [0.3.0](https://github.com/IjzerenHein/react-navigation-shared-element/compare/v0.2.1...v0.3.0) (2019-08-29)


### Initial release
