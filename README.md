# Awesome Tiny JS with stars

<div align="center">
  <a href="https://github.com/thoughtspile/awesome-tiny-js#readme">
    <img src="./awesome-logo.png" width="300" height="207">
  </a>
</div>

Tiny front-end libraries to put your bundle on a diet. Rules:

* Size is under 2 kB-ish, min + gzip, with all dependencies, except where noted.
* For multi-purpose libraries, the size of a useful subset must be under 2 kB-ish.
* Useful client-side. I haven't figured out participation rules for node-only libraries, and I'm not too worried about them.
* Second-level libraries only allowed for React, Vue, Angular, svelte.
* 100+ GitHub stars *or* 500+ weekly npm installs to focus on tools with some community review.
* No zero-JS (CSS- or type-only) libraries. It's not awesome-css or something.

## Contents

* [UI Frameworks](#ui-frameworks)
* [Event Emitters](#event-emitters)
* [State Managers](#state-managers)
  * [Signals](#signals)
  * [Reactive Programming](#reactive-programming)
* [Routers and URL Utils](#routers-and-url-utils)
* [API Layer](#api-layer)
* [I18N](#i18n)
* [Dates and Time](#dates-and-time)
* [Generic Utilities](#generic-utilities)
* [Validation](#validation)
* [Unique ID Generation](#unique-id-generation)
* [Colors](#colors)
* [Touch Gestures](#touch-gestures)
* [Text Search](#text-search)

## UI Frameworks

UI frameworks (libraries?) provide declarative templates, event bindings, and observable state to update the view. I've been generous and expanded the size limit for this category to 4.5 kB (if you're boring, count them as 2 libraries), but also increased the star limit to 2K.

* [preact](https://github.com/preactjs/preact) ⭐ 38,820 | 🐛 39 | 🌐 JavaScript | 📅 2026-08-13 - React-like API (pre-hooks). Cool ecosystem of similarly tiny tools and components. Highly recommended. <img align="top" height="24" src="./img/preact.svg">

The following libraries are small and cool, but note they're about [500x less popular than preact.](https://npmtrends.com/preact-vs-hyperapp-vs-redom) Kudos for deconstrucing the very essence of a "framework":

* [hyperapp](https://github.com/jorgebucaran/hyperapp) ⭐ 19,201 | 🐛 14 | 🌐 JavaScript | 📅 2025-03-20 - vDOM framework with pure JS syntax and immutable state, <img align="top" height="24" src="./img/hyperapp.svg">
* [redom](https://github.com/redom/redom) ⭐ 3,432 | 🐛 9 | 🌐 JavaScript | 📅 2025-03-10 - Hyperapp-style templates with *imperative* event listeners and updates, <img align="top" height="24" src="./img/redom.svg">

Now, for the [openly experimental](https://npmtrends.com/@arrow-js/core-vs-fre-vs-hyperapp-vs-redom-vs-superfine-vs-vanjs-core) UI libraries:

* [van](https://github.com/vanjs-org/van) ⭐ 4,422 | 🐛 40 | 🌐 JavaScript | 📅 2026-07-16 - vDOM-based framework optimized for no-build setups, <img align="top" height="24" src="./img/vanjs-core.svg">
* [fre](https://github.com/frejs/fre) ⭐ 3,766 | 🐛 10 | 🌐 JavaScript | 📅 2026-08-09 - React-like library with hooks and concurrency, <img align="top" height="24" src="./img/fre.svg">
* [arrowjs](https://github.com/justin-schroeder/arrow-js) ⭐ 3,721 | 🐛 6 | 🌐 TypeScript | 📅 2026-07-01 - Tagged templates + reactive data, <img align="top" height="24" src="./img/arrow-jscore.svg">
* [superfine](https://github.com/jorgebucaran/superfine) ⭐ 1,596 | 🐛 5 | 🌐 JavaScript | 📅 2022-08-16 - Hyperapp with state & effect hooks removed, <img align="top" height="24" src="./img/superfine.svg">

And if being declarative is not your thing:

* [umbrella](https://github.com/franciscop/umbrella) ⭐ 2,344 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-02 - jQuery-style DOM manipulation library, <img align="top" height="24" src="./img/umbrellajs.svg">

## Event Emitters

Event emitter pattern is fairly easy to implement yourself, but why bother when you have these cool tools? With an arms race to build the smallest one, the limit is 0.5 kB.

* [mitt](https://github.com/developit/mitt) ⭐ 11,899 | 🐛 27 | 🌐 TypeScript | 📅 2024-08-14 - Plain event emitter that I use on most projects, <img align="top" height="24" src="./img/mitt.svg">
* [nanoevents](https://github.com/ai/nanoevents) ⭐ 1,631 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-22 - Nicer unsubscribe API, but no `*` event, <img align="top" height="24" src="./img/nanoevents.svg">
* [onfire.js](https://github.com/hustcc/onfire.js) ⭐ 496 | 🐛 0 | 🌐 TypeScript | 📅 2019-04-22 - Also has `.once` method, <img align="top" height="24" src="./img/onfirejs.svg">

## State Managers

State managers combine observable state with actions and framework bindings, intended for app-wide state.

* [zustand](https://github.com/pmndrs/zustand) ⭐ 58,574 | 🐛 3 | 🌐 TypeScript | 📅 2026-08-13 - Simple stores with pleasant actions and selectors. Vanilla <img align="top" height="24" src="./img/zustandvanilla.svg">, React <img align="top" height="24" src="./img/zustand.svg">
* [nanostores](https://github.com/nanostores/nanostores) ⭐ 7,556 | 🐛 22 | 🌐 TypeScript | 📅 2026-08-15 - Modular store with good tree-shaking support, <img align="top" height="24" src="./img/nanostores.svg"> vanilla, + React <img align="top" height="24" src="./img/nanostoresreact.svg"> extra. Supports all the top frameworks.
* [unistore](https://github.com/developit/unistore) ⭐ 2,847 | 🐛 46 | 🌐 JavaScript | 📅 2021-06-07 - Centralized store with actions, <img align="top" height="24" src="./img/unistore.svg"> + React <img align="top" height="24" src="./img/unistorereact.svg">
* [storeon](https://github.com/storeon/storeon) ⭐ 1,976 | 🐛 15 | 🌐 JavaScript | 📅 2024-12-10 - Minimal redux-styled store with lots of framework connectors, <img align="top" height="24" src="./img/storeon.svg">. React extra <img align="top" height="24" src="./img/storeonreact.svg"> + Vue, Svelte, Angular.
* [teaful](https://github.com/teafuljs/teaful) ⭐ 712 | 🐛 18 | 🌐 TypeScript | 📅 2026-04-09 - Store with useState-like API, <img align="top" height="24" src="./img/teaful.svg">, including React / preact connector.
* [exome](https://github.com/marcisbee/exome) ⭐ 281 | 🐛 1 | 🌐 TypeScript | 📅 2026-01-29 - Atomic stores with lots of framework connectors, <img align="top" height="24" src="./img/exome.svg"> + React <img align="top" height="24" src="./img/exomereact.svg"> extra. Supports all the top frameworks.

### Signals

A signal-styled state manager provides observable values (aka *signals*), derived values and effects.

* [@preact/signals](https://github.com/preactjs/signals) ⭐ 4,473 | 🐛 42 | 🌐 TypeScript | 📅 2026-08-14 - The OG signals from preact <img align="top" height="24" src="./img/preactsignals-core.svg"> core, <img align="top" height="24" src="./img/preactsignals-react.svg"> with react integration.
* [hyperactiv](https://github.com/elbywan/hyperactiv) ⭐ 446 | 🐛 8 | 🌐 JavaScript | 📅 2026-06-21 - 4 functions to make objects observable and listen to changes, <img align="top" height="24" src="./img/hyperactiv.svg">
* [usignal](https://github.com/WebReflection/usignal) ⭐ 268 | 🐛 1 | 🌐 JavaScript | 📅 2026-05-28 - A smaller signal implementation, <img align="top" height="24" src="./img/usignal.svg">
* [flimsy](https://github.com/fabiospampinato/flimsy) ⭐ 193 | 🐛 1 | 🌐 TypeScript | 📅 2026-07-17 - Signals from Solid (it *almost* fit into UI frameworks category itself). Author warning: *it's probably buggy.* <img align="top" height="24" src="./img/flimsy.svg">

Honorable mention: [oby](https://github.com/vobyjs/oby) ⭐ 245 | 🐛 5 | 🌐 JavaScript | 📅 2026-07-17 *could* make it *if* it had tree-shaking, but otherwise is around 7 kB.

### Reactive Programming

Another well-known state management approach is reactive programmning — operating on event streams, applying filters and transforms to end up with an observable value. Think RxJS, but tiny:

* [callbag-basics](https://github.com/staltz/callbag-basics) ⭐ 1,652 | 🐛 8 | 🌐 JavaScript | 📅 2023-04-20 - Rx-style event streams, <img align="top" height="24" src="./img/callbag-basics.svg">
* [flyd](https://github.com/paldepind/flyd) ⭐ 1,565 | 🐛 55 | 🌐 JavaScript | 📅 2024-02-05 - Rx-styled event streams, <img align="top" height="24" src="./img/flyd.svg">

## Routers and URL Utils

Do stuff on URL / history changes, with path matching and parsing:

* [wouter](https://github.com/molefrog/wouter) ⭐ 7,865 | 🐛 30 | 🌐 TypeScript | 📅 2026-08-10 - Declarative router for React / preact, <img align="top" height="24" src="./img/wouter.svg">, also available as a standalone hook: <img align="top" height="24" src="./img/wouteruse-browser-location.svg">
* [navaid](https://github.com/lukeed/navaid) ⭐ 796 | 🐛 7 | 🌐 JavaScript | 📅 2024-01-20 - History-based observable router, <img align="top" height="24" src="./img/navaid.svg">
* [@nanostores/router](https://github.com/nanostores/router) ⭐ 326 | 🐛 4 | 🌐 TypeScript | 📅 2026-07-23 - Routes as a nanostores store (framework-agnostic), <img align="top" height="24" src="./img/nanostoresrouter.svg">

Just want to parse or match URL paths without observing them? Here you go:

* [regexparam](https://github.com/lukeed/regexparam) ⭐ 597 | 🐛 9 | 🌐 JavaScript | 📅 2023-12-03 - Convert path to regexp in <img align="top" height="24" src="./img/regexparam.svg">
* [qss](https://github.com/lukeed/qss) ⭐ 452 | 🐛 5 | 🌐 JavaScript | 📅 2023-03-10 - Parse querystrings in <img align="top" height="24" src="./img/qss.svg">. Not sure you need it, [URL API](https://developer.mozilla.org/en-US/docs/Web/API/URL) support is good.
* [matchit](https://github.com/lukeed/matchit) ⭐ 323 | 🐛 3 | 🌐 JavaScript | 📅 2021-11-03 - Route parser and matcher in <img align="top" height="24" src="./img/matchit.svg">

## API Layer

`fetch` API has some boilerplate associated with it: serialize & parse data, reject on non-200 response, etc. These tiny packages handle it for you:

* [wretch](https://github.com/elbywan/wretch) ⭐ 5,179 | 🐛 10 | 🌐 TypeScript | 📅 2026-06-19 - Chainable API with error processing and lots of extra plugins, <img align="top" height="24" src="./img/wretch.svg">
* [redaxios](https://github.com/developit/redaxios) ⭐ 4,880 | 🐛 34 | 🌐 JavaScript | 📅 2023-08-15 - Drop-in axios replacement for modern browsers, <img align="top" height="24" src="./img/redaxios.svg">
* [gretchen](https://github.com/truework/gretchen) ⭐ 328 | 🐛 17 | 🌐 TypeScript | 📅 2023-10-05 - Chainable API with type-safe errors, <img align="top" height="24" src="./img/gretchen.svg">

If for some reason you still need a fetch polyfill, try this one:

* [unfetch](https://github.com/developit/unfetch) ⭐ 5,700 | 🐛 30 | 🌐 JavaScript | 📅 2023-07-23 - Loose fetch polyfill, <img align="top" height="24" src="./img/unfetch.svg">

## I18N

A map of strings might seem enough to translate an app, but these tools also handle interpolation and some extra goodies:

* [lingui](https://github.com/lingui/js-lingui) ⭐ 5,846 | 🐛 65 | 🌐 TypeScript | 📅 2026-08-14 - Small core with template strings, <img align="top" height="24" src="./img/linguicore.svg">
* [rosetta](https://github.com/lukeed/rosetta) ⭐ 797 | 🐛 6 | 🌐 JavaScript | 📅 2024-01-20 - Bare-bones template strings (`{{hello}}, {{username}}`) and custom functions for everyting else, <img align="top" height="24" src="./img/rosetta.svg">
* [eo-locale](https://github.com/ibitcy/eo-locale) ⭐ 347 | 🐛 13 | 🌐 TypeScript | 📅 2024-12-10 - Interpolation and dates / numbers, <img align="top" height="24" src="./img/eo-localecore.svg">, or <img align="top" height="24" src="./img/eo-localereact.svg"> with react bindings.
* [@nanostores/i18n](https://github.com/nanostores/i18n) ⭐ 305 | 🐛 5 | 🌐 TypeScript | 📅 2026-07-23 - Detect locale, load dictionaries, format dates / numbers, <img align="top" height="24" src="./img/nanostoresin.svg"> including nanostores.

## Dates and Time

Date and time manipulation in pure JS is verbose. Luckily, two of the top date libraries have sensible size:

* [dayjs](https://github.com/iamkun/dayjs) ⭐ 48,665 | 🐛 1,297 | 🌐 JavaScript | 📅 2026-08-16 - *Almost* moment.js-compatible API, covers most use cases, <img align="top" height="24" src="./img/dayjsesm.svg">
* [date-fns](https://github.com/date-fns/date-fns/) ⭐ 36,625 | 🐛 992 | 🌐 TypeScript | 📅 2026-08-10 - Not tiny as a whole, but [most functions](https://bundlephobia.com/package/date-fns) are under 1 kB each (format and parse are quite heavy).

And some more packages that only do formatting:

* [ms](https://github.com/vercel/ms) ⭐ 5,544 | 🐛 35 | 🌐 TypeScript | 📅 2026-05-20 - Parse & format ms durations, e.g. `"1m" <-> 60000`, <img align="top" height="24" src="./img/ms.svg">
* [timeago.js](https://github.com/hustcc/timeago.js) ⭐ 5,370 | 🐛 9 | 🌐 TypeScript | 📅 2026-06-30 - Format dates into stuff like *X minutes ago* or *in X hours,* <img align="top" height="24" src="./img/timeagojs.svg">
* [tinytime](https://github.com/aweary/tinytime) ⭐ 1,323 | 🐛 19 | 🌐 JavaScript | 📅 2023-01-12 - Simple date / time formatter: `{h}:{mm} -> 9:33`, <img align="top" height="24" src="./img/tinytime.svg">
* [tinydate](https://github.com/lukeed/tinydate) ⭐ 1,067 | 🐛 2 | 🌐 JavaScript | 📅 2024-01-20 - Date / time formatter, only supports padded numeric output (`September -> 09`), <img align="top" height="24" src="./img/tinydate.svg">
* [fromnow](https://github.com/lukeed/fromnow) ⭐ 186 | 🐛 2 | 🌐 JavaScript | 📅 2019-07-08 - More of the same, <img align="top" height="24" src="./img/fromnow.svg">
* [time-stamp](https://github.com/jonschlinkert/time-stamp) ⭐ 110 | 🐛 8 | 🌐 JavaScript | 📅 2020-11-24 - More of the same, <img align="top" height="24" src="./img/time-stamp.svg">

Note that the built-in [`Intl.DateTimeFormat`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat) has decent support.

## Generic Utilities

Something you'd find in lodash or ramda, but smaller. Most are pretty similar and very small, with minor differences in package structure (single / package-per-helper) and tree shaking vs direct helper import.

* [just](https://github.com/angus-c/just) ⭐ 6,203 | 🐛 58 | 🌐 JavaScript | 📅 2024-02-11 - 82 helpers in separate packages [(list).](https://anguscroll.com/just/)
* [remeda](https://github.com/remeda/remeda) ⭐ 5,414 | 🐛 16 | 🌐 TypeScript | 📅 2026-08-16 - 90 tree-shakable helpers [(list).](https://bundlephobia.com/package/remeda)
* [rambda](https://github.com/selfrefactor/rambda) ⭐ 1,755 | 🐛 1 | 🌐 JavaScript | 📅 2026-08-13 - 187 tree-shakable helpers [(list).](https://bundlephobia.com/package/rambda)
* [@fxts/core](https://github.com/marpple/FxTS) ⭐ 1,165 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-08 - 96 tree-shakable helpers. Lazy evaluation support.

Honorable mention: [underscore,](https://github.com/jashkenas/underscore) ⭐ 27,337 | 🐛 52 | 🌐 JavaScript | 📅 2026-08-12 contains many sub-1 kB helpers. It does not tree-shake as well as the libraries above due to codebase structure.

Note: lodash itself is not tree-shakable, but has made many attempts at modulaity with `lodash.method` packages, imports from `lodash/method`, and `lodash-es`, none of which work well in practice.

Also note that much of the original lodash functionality comes built-in with modern ES. Prefer native versions over libraries as your browser target allows.

## Validation

To check if an object matches an expected schema, you'd often use zod, yup, joi or ajv. But 90% of the time you can get what you need in under 2 kB. *Note:* I compare a base validation subset (core + object / array + string / number / boolean) under tree-shaking to avoid punishing libs that have more features.

* [valibot](https://github.com/fabian-hiller/valibot) ⭐ 8,931 | 🐛 172 | 🌐 TypeScript | 📅 2026-08-16 - Another modular validation library, <img align="top" height="24" src="./img/valibot.svg">
* [superstruct](https://github.com/ianstormtaylor/superstruct) ⭐ 7,137 | 🐛 103 | 🌐 TypeScript | 📅 2024-10-01 - The most popular modular validation library with good tree-shaking, <img align="top" height="24" src="./img/superstruct.svg">
* [v8n](https://github.com/imbrn/v8n) ⭐ 4,143 | 🐛 0 | 🌐 JavaScript | 📅 2025-01-01 - zod-style API with fine-grained checks: `v8n().string().minLength(5).first("H").last("o")`. No tree shaking, <img align="top" height="24" src="./img/vn.svg">
* [deep-waters](https://github.com/antonioru/deep-waters) ⭐ 202 | 🐛 16 | 🌐 JavaScript | 📅 2023-01-06 - Composable functional validators, <img align="top" height="24" src="./img/deep-waterscompose-deep-watershasShape-deep-watersarrayOf-deep-watersisString-deep-watersisNumber-deep-watersisBoolean.svg">.
* [banditypes](https://github.com/thoughtspile/banditypes) ⭐ 183 | 🐛 3 | 🌐 JavaScript | 📅 2026-07-08 - The smallest validation library: <img align="top" height="24" src="./img/banditypes.svg">

## Unique ID Generation

Unique ID generation does not take a lot of code, but it's not someting I'd want to write myself. Limit is 500 bytes. Also note that the [native `crypto.randomUUID`](https://developer.mozilla.org/en-US/docs/Web/API/Crypto/randomUUID) has [OK support.](https://caniuse.com/mdn-api_crypto_randomuuid)

* [nanoid](https://github.com/ai/nanoid) ⭐ 26,935 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-10 - Random IDs with larger alphabet, <img align="top" height="24" src="./img/nanoid.svg">
* [uid](https://github.com/lukeed/uid) ⭐ 667 | 🐛 2 | 🌐 JavaScript | 📅 2024-09-27 - More of the same, <img align="top" height="24" src="./img/uid.svg">
* [@lukeed/uuid](https://github.com/lukeed/uuid) ⭐ 409 | 🐛 4 | 🌐 JavaScript | 📅 2024-09-27 - Real UUIDs, <img align="top" height="24" src="./img/lukeeduuid.svg">
* [hexoid](https://github.com/lukeed/hexoid) ⭐ 204 | 🐛 2 | 🌐 JavaScript | 📅 2026-05-04 - Hexadecimal IDs, <img align="top" height="24" src="./img/hexoid.svg">

## Colors

Color manipulation is rare in pure UI development, but very helpful for data visualization, and uses [freaky math.](https://en.wikipedia.org/wiki/HSL_and_HSV#Color_conversion_formulae) Don't fry your brain, take these:

* [randomcolor](https://github.com/davidmerfield/randomColor) ⭐ 6,125 | 🐛 16 | 🌐 JavaScript | 📅 2025-12-03 - Attractive random colors with configuration. <img align="top" height="24" src="./img/randomcolor.svg">
* [colord](https://github.com/omgovich/colord) ⭐ 1,879 | 🐛 36 | 🌐 TypeScript | 📅 2026-05-23 - Manipulate colors and convert between spaces, <img align="top" height="24" src="./img/colord.svg">. Extra features come as plugins, 150b to 1.5 kB each.
* [polychrome](https://github.com/cdonohue/polychrome) ⭐ 288 | 🐛 6 | 🌐 TypeScript | 📅 2018-02-11 - More of the same, <img align="top" height="24" src="./img/polychrome.svg">
* [colr](https://github.com/stayradiated/colr) ⭐ 106 | 🐛 1 | 🌐 JavaScript | 📅 2020-05-07 - More of the same, <img align="top" height="24" src="./img/colr.svg" >

## Touch Gestures

Touch gestures like swipe, drag, pinch or doubletap are a staple of mobile UX, but recognizing a series of touchmove / pointer events as a gesture is tricky, and testing is painful. Here are two libraries that do the heavy lifting for you:

* [alloyfinger](https://github.com/AlloyTeam/AlloyFinger) ⭐ 3,439 | 🐛 77 | 🌐 JavaScript | 📅 2019-01-03 - Pan, swipe, tap, doubletap, longpress, *and* pinch / rotate. My personal favorite. <img align="top" height="24" src="./img/alloyfinger.svg">.
* [tinygesture](https://github.com/sciactive/tinygesture) ⭐ 228 | 🐛 2 | 🌐 TypeScript | 📅 2026-04-04 - Configurable pan, swipe, tap, doubletap, longpress. <img align="top" height="24" src="./img/tinygesture.svg">.

Even if you want to detect gestures yourself, juggling mouse, touch and pointer events is hard enough, and browser inconsistencies don't help. Here are two more libraries to assist with that:

* [detect-it](https://github.com/rafgraph/detect-it) ⭐ 434 | 🐛 1 | 🌐 TypeScript | 📅 2021-05-02 - Detect present and primary input method (touch / mouse) and supported events, <img align="top" height="24" src="./img/detect-it.svg">
* [pointer-tracker](https://github.com/GoogleChromeLabs/pointer-tracker) ⚠️ Archived - Unified interface for mouse, touch and pointer events, <img align="top" height="24" src="./img/pointer-tracker.svg">

Honorable mentions: [any-touch](https://github.com/any86/any-touch) ⭐ 1,246 | 🐛 18 | 🌐 TypeScript | 📅 2026-01-09 attempts a modular approach to gesture detection, but the core is around 2 kB without any gesture recognizers. [rc-gesture,](https://github.com/react-component/gesture) ⭐ 104 | 🐛 15 | 🌐 TypeScript | 📅 2021-07-27 used in ant design system, could be the only react component on the list, but babel-runtime / corejs polyfills hard-wired into the build push the \~2.5 kB size to over 10 kB.

## Text Search

Text search is important for client-side filtering and autosuggests. Naive `option.includes(search)` has no sensible order on the results, and ignoring word boundaries gives unexpected matches like *spa -> newSPAper.* First, here are some libraries that prioritize word matches:

* [wade](https://github.com/kbrsh/wade) ⭐ 2,955 | 🐛 7 | 🌐 JavaScript | 📅 2023-05-13 - Also similar, [(compare)](https://leeoniya.github.io/uFuzzy/demos/compare.html?libs=js-search,Wade,ndx\&search=twilight%20sag) <img align="top" height="24" src="./img/wade.svg">
* [js-search](https://github.com/bvaughn/js-search) ⭐ 2,219 | 🐛 8 | 🌐 JavaScript | 📅 2023-05-12 - Feature-rich and customizable: multi-field indices, stop words, custom stemmers and tokenizers. <img align="top" height="24" src="./img/js-search.svg">
* [libsearch](https://github.com/thesephist/libsearch) ⭐ 388 | 🐛 1 | 🌐 JavaScript | 📅 2022-07-21 - Index-free search (slower, but easier to use) with sane ordering <img align="top" height="24" src="./img/libsearch.svg">
* [ndx](https://github.com/localvoid/ndx) ⭐ 157 | 🐛 1 | 🌐 TypeScript | 📅 2023-03-15 - Similar to js-search, differs in [ranking](https://kmwllc.com/index.php/2020/03/20/understanding-tf-idf-and-bm-25/) and is less strict for multi-word queries [(compare)](https://leeoniya.github.io/uFuzzy/demos/compare.html?libs=js-search,ndx,Wade\&search=twilight%20sag). Supports field weights. <img align="top" height="24" src="./img/ndx-ndxquery.svg">

One way to find sensible inexact matches is *stemming* — converting words to a root form. *Walked* will match *walking,* etc. Here are a few [Porter stemmers](https://vijinimallawaarachchi.com/2017/05/09/porter-stemming-algorithm/) for English language:

* [stemmer](https://github.com/words/stemmer) ⭐ 138 | 🐛 0 | 🌐 JavaScript | 📅 2022-11-02 - <img align="top" height="24" src="./img/stemmer.svg">
* [porter-stemmer](https://github.com/jedp/porter-stemmer) ⭐ 102 | 🐛 4 | 🌐 JavaScript | 📅 2020-09-30 - <img align="top" height="24" src="./img/porter-stemmer.svg">

For non-English words, I only have honorable mentions: [snowball-js](https://github.com/fortnightlabs/snowball-js) ⭐ 102 | 🐛 3 | 🌐 JavaScript | 📅 2011-03-09 is 17 kB with 15 languages, [lunr-languages](https://github.com/MihaiValentin/lunr-languages) ⭐ 457 | 🐛 17 | 🌐 JavaScript | 📅 2026-08-09 supports 30 languages but only works with [lunr,](https://github.com/olivernn/lunr.js) ⭐ 9,199 | 🐛 130 | 🌐 JavaScript | 📅 2024-07-31 the most promising one is [natural](https://github.com/NaturalNode/natural/tree/master/lib/natural/stemmers) ⭐ 10,878 | 🐛 86 | 🌐 JavaScript | 📅 2026-02-22 but it depends on Node.js.

### Fuzzy search

**Fuzzy search** is another take on inexact matching — the words can be modified. First, we have libraries that only allow insertion: spacecat -> SPACECrAfT. Not perfect for general-purpose text search, but great for filename, command, or URL lookups.

* [fuzzysearch](https://github.com/bevacqua/fuzzysearch) ⭐ 2,742 | 🐛 5 | 🌐 JavaScript | 📅 2023-05-31 -  One string at a time, does not compute score / rank. <img align="top" height="24" src="./img/fuzzysearch.svg">
* [fuzzy](https://github.com/mattyork/fuzzy) ⭐ 835 | 🐛 29 | 🌐 JavaScript | 📅 2021-12-20 - Index-free, can highlight matches. <img align="top" height="24" src="./img/fuzzy.svg">
* [liquidmetal](https://github.com/rmm5t/liquidmetal) ⭐ 293 | 🐛 1 | 🌐 JavaScript | 📅 2020-06-17 - Quicksilver algorithm, prioritizes matches at start of word for command abbreviations (e.g. `gp` -> `git push`). One string at a time. <img align="top" height="24" src="./img/liquidmetal.svg">
* [fuzzy-search](https://github.com/wouterrutgers/fuzzy-search) ⭐ 229 | 🐛 16 | 🌐 JavaScript | 📅 2023-03-14 - With stateful index. <img align="top" height="24" src="./img/fuzzy-search.svg">
* [quick-score](https://github.com/fwextensions/quick-score) ⭐ 164 | 🐛 6 | 🌐 JavaScript | 📅 2023-01-08 - Another quicksilver-based lib, tweaked for long strings. Built-in list filtering and sorting, <img align="top" height="24" src="./img/quick-score.svg"> or 1.2 kB for single-string scoring.
* [fzy.js](https://github.com/jhawthorn/fzy.js) ⭐ 163 | 🐛 2 | 🌐 JavaScript | 📅 2024-09-24 - Matches one string at a time, tree-shakeable scores and match highlighting. <img align="top" height="24" src="./img/fzyjs.svg"> total, or \~150 bytes for `hasMatch` only.

Finally, one library is specifically built for spellchecking:

* [fuzzyset](https://github.com/Glench/fuzzyset.js) ⭐ 1,375 | 🐛 1 | 🌐 JavaScript | 📅 2021-12-13 - Find misspellings, e.g. missipissi -> Missisipi, <img align="top" height="24" src="./img/fuzzyset.svg"> Commercial usage costs $42.

## Contributing

Suggestions welcome! See [contributing.md](contributing.md), or drop an [issue](https://github.com/thoughtspile/awesome-tiny-js/issues) ⭐ 776 | 🐛 5 | 🌐 JavaScript | 📅 2024-09-24.

## Footnotes

See [WIP](wip.md) for possibly awesome libraries I have found, but not yet analyzed deeply, and [incubate](incubate.md) for awesome libraries that don't meet popularity criteria yet.

Collected and reviewed by [Vladimir Klepov](https://blog.thoughtspile.tech) in 2023.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-16._
