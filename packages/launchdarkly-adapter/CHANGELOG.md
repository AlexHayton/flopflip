# @flopflip/launchdarkly-adapter

## 3.0.0

### Major Changes

- [`891fb29`](https://github.com/tdeekens/flopflip/commit/891fb294d5d6e016224b5a16d22760f0a55f9606) [#1287](https://github.com/tdeekens/flopflip/pull/1287) Thanks [@renovate](https://github.com/apps/renovate)! - flopflip is now built with TypeScript v4 which can cause compatibility issues if you project runs on an older version of TypeScript

### Patch Changes

- Updated dependencies [[`891fb29`](https://github.com/tdeekens/flopflip/commit/891fb294d5d6e016224b5a16d22760f0a55f9606)]:
  - @flopflip/types@3.0.0

## 2.15.7

### Patch Changes

- [`5598832`](https://github.com/tdeekens/flopflip/commit/5598832df710f707fe0832cd4011e26c060e24a8) [#1275](https://github.com/tdeekens/flopflip/pull/1275) Thanks [@tdeekens](https://github.com/tdeekens)! - chore: update deps

## 2.15.6

### Patch Changes

- [`eac3bd4`](https://github.com/tdeekens/flopflip/commit/eac3bd4d80fee4209ed39d7b9199916afb7f192f) [#1269](https://github.com/tdeekens/flopflip/pull/1269) Thanks [@tdeekens](https://github.com/tdeekens)! - chore: update dependencies across packages

- Updated dependencies [[`eac3bd4`](https://github.com/tdeekens/flopflip/commit/eac3bd4d80fee4209ed39d7b9199916afb7f192f)]:
  - @flopflip/types@2.5.10

## 2.15.5

### Patch Changes

- Updated dependencies [[`8c97b10`](https://github.com/tdeekens/flopflip/commit/8c97b10ce7159e8769791834bf6d7a1b5aba37f3)]:
  - @flopflip/types@2.5.9

## 2.15.4

### Patch Changes

- Updated dependencies [[`651a0ac`](https://github.com/tdeekens/flopflip/commit/651a0ac187860c9511d7da0bbf7cde6f5a9bb5aa)]:
  - @flopflip/types@2.5.8

## 2.15.3

### Patch Changes

- [`407f8e7`](https://github.com/tdeekens/flopflip/commit/407f8e7484ef25316d34f14f29b94c673ecd8aed) [#1235](https://github.com/tdeekens/flopflip/pull/1235) Thanks [@tdeekens](https://github.com/tdeekens)! - chore: update deps and migrate to TypeScript v4

* [`407f8e7`](https://github.com/tdeekens/flopflip/commit/407f8e7484ef25316d34f14f29b94c673ecd8aed) [#1235](https://github.com/tdeekens/flopflip/pull/1235) Thanks [@tdeekens](https://github.com/tdeekens)! - chore: update deps

* Updated dependencies [[`407f8e7`](https://github.com/tdeekens/flopflip/commit/407f8e7484ef25316d34f14f29b94c673ecd8aed)]:
  - @flopflip/types@2.5.7

## 2.15.2

### Patch Changes

- [`de8c944`](https://github.com/tdeekens/flopflip/commit/de8c944a76b5fb7185f4eccb70bb40920c3cccb0) [#1225](https://github.com/tdeekens/flopflip/pull/1225) Thanks [@tdeekens](https://github.com/tdeekens)! - fix: to check subscription of flag upon initial sdk fetch

## 2.15.1

### Patch Changes

- [`6034a1c`](https://github.com/tdeekens/flopflip/commit/6034a1c8ff2c166f3fabee1deac86cf6262edde3) [#1214](https://github.com/tdeekens/flopflip/pull/1214) Thanks [@tdeekens](https://github.com/tdeekens)! - refactor(cypress-plugin): type the global flopflip

- Updated dependencies [[`6034a1c`](https://github.com/tdeekens/flopflip/commit/6034a1c8ff2c166f3fabee1deac86cf6262edde3)]:
  - @flopflip/types@2.5.6

## 2.15.0

### Minor Changes

- [`3ef69dd`](https://github.com/tdeekens/flopflip/commit/3ef69dde568307a57ab6254f699eb5fe1d10f476) [#1210](https://github.com/tdeekens/flopflip/pull/1210) Thanks [@tdeekens](https://github.com/tdeekens)! - feat: to expose adapters globally

  Exposing adapters globally simplifies a lot of integrations we can perform. Each adapter gets a namespace according to its `TAdapterInterfaceIdentifiers`. So we have `launchdarkly`, `memory`, etc on the `__flopflip__` global namespace.

  We use the `globalThis` polyfill and TC39 spec to correctly determine the global this in any context and assign each adapter instance as `adapter` and `updateFlags`.

  This means you could do `window.__flopflip__.launchdarkly.updateFlags` now.

  With the next version of the `cypress-plugin` we also simplify the API. As we're not `1.x.x` we don't consider it breaking. You now have to pass an `TAdapterInterfaceIdentifiers` so that the plugin can correlate the adapter internally. This means you could do

  ```diff
  +addCommands({ adapterId: 'launchdarkly' })
  -addCommands({ adapter: adapter, updateFlags, updateFlags })
  ```

## 2.14.5

### Patch Changes

- [`b4dd923`](https://github.com/tdeekens/flopflip/commit/b4dd92356208ffe1feefea0a86f7c05d738fcabb) [#1208](https://github.com/tdeekens/flopflip/pull/1208) Thanks [@tdeekens](https://github.com/tdeekens)! - fix: types dependency

## 2.14.4

### Patch Changes

- [`8f7e504`](https://github.com/tdeekens/flopflip/commit/8f7e504951cb2dcb6b86abaa4908d10314515860) [#1206](https://github.com/tdeekens/flopflip/pull/1206) Thanks [@tdeekens](https://github.com/tdeekens)! - feat(launchdarkly-adapter): add unsubcribe flag state

- Updated dependencies [[`8f7e504`](https://github.com/tdeekens/flopflip/commit/8f7e504951cb2dcb6b86abaa4908d10314515860)]:
  - @flopflip/types@2.5.5

## 2.14.3

### Patch Changes

- [`52ccb88`](https://github.com/tdeekens/flopflip/commit/52ccb880b7a2948ff3ee46b3f51613be6a99ee3f) [#1204](https://github.com/tdeekens/flopflip/pull/1204) Thanks [@tdeekens](https://github.com/tdeekens)! - refactor(launchdarkly-adapter): to use emitter

## 2.14.2

### Patch Changes

- [`9460803`](https://github.com/tdeekens/flopflip/commit/9460803fb19339c015077c888141c4322d1b598c) [#1198](https://github.com/tdeekens/flopflip/pull/1198) Thanks [@tdeekens](https://github.com/tdeekens)! - fix: export of updateFlags re-export edition

## 2.14.1

### Patch Changes

- [`4150b1d`](https://github.com/tdeekens/flopflip/commit/4150b1dfc8e022ffcc8055f061be14a400ac62ae) [#1196](https://github.com/tdeekens/flopflip/pull/1196) Thanks [@tdeekens](https://github.com/tdeekens)! - fix: export of updateFlags

## 2.14.0

### Minor Changes

- [`17bbc54`](https://github.com/tdeekens/flopflip/commit/17bbc545dd476728a5bdedc566b46ec9cc3753c1) [#1189](https://github.com/tdeekens/flopflip/pull/1189) Thanks [@tdeekens](https://github.com/tdeekens)! - feat: add the notion of locked flags and `updateFlags` to 3 out of 4 adapters

  The three adapters `launchdarkly-adapter`, `localstorage-adapter` and `memory-adapter` now expose a `updateFlags` method.

  You can now:

  ```js
  import { updateFlags } from '@flopflip/launchdarkly-adapter';

  updateFlags({ myFlag: true });
  ```

  which will internally set the flag value of `myFlag` to `true` and lock the flag from changing via the LaunchDarkly API. You can pass `{ lockFlags: false }` as an second argument to keep flag updates.

  The same applied for the `localstorage-adapter` adapter. Where updating a flag will not yield it being locked but you can opt-in via `{ lockFlags: true }`. So far only the `launchdarkly-adapter` locks flags by default when using `updateFlags`. This default is sensible as flag value can easily be overwritten by the LaunchDarkly socket connection giving an update.

## 2.13.4

### Patch Changes

- [`76354f8`](https://github.com/tdeekens/flopflip/commit/76354f8bd034b0ece14374b5eddf39858f75c7a7) [#1143](https://github.com/tdeekens/flopflip/pull/1143) Thanks [@tdeekens](https://github.com/tdeekens)! - chore: update deps

- Updated dependencies [[`76354f8`](https://github.com/tdeekens/flopflip/commit/76354f8bd034b0ece14374b5eddf39858f75c7a7)]:
  - @flopflip/types@2.5.4

## 2.13.3

### Patch Changes

- [`32cc6a8`](https://github.com/tdeekens/flopflip/commit/32cc6a823ff9812ab2f256b69dd3f46e273feb5e) [#1102](https://github.com/tdeekens/flopflip/pull/1102) Thanks [@tdeekens](https://github.com/tdeekens)! - Update dependencies (TypeScript 3.9)

- Updated dependencies [[`32cc6a8`](https://github.com/tdeekens/flopflip/commit/32cc6a823ff9812ab2f256b69dd3f46e273feb5e)]:
  - @flopflip/types@2.5.3
