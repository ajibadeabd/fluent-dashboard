## Installation

First of all, make sure you have all prerequisites installed:
- [Node.js](https://nodejs.org/en/) (>=8.9)
- [npm](https://www.npmjs.com/get-npm) version 3+ (or [yarn](https://yarnpkg.com/lang/en/docs/install/#mac-stable) version 1.16+)
- [Docker](https://docker.com)




After checking the prerequisites, follow these simple steps to install and use Fluentbit Dashboard:

```
docker run -ti -p 127.0.0.1:2020:2020 fluent/fluent-bit:1.4 /fluent-bit/bin/fluent-bit -H -i cpu  -i cpu -o stdout -f 1
```

```
$ npm install

# serve with hot reload at localhost:8080 by default.
$ npm run serve

# build for production
$ npm run build

# build for production and view the bundle analyzer report.
$ npm run build --report
```

If you use yarn:
```
$ yarn install

# serve with hot reload at localhost:8080 by default.
$ yarn serve

# build for production
$ yarn build

# build for production and view the bundle analyzer report.
$ yarn build --report
```

## Features
[Responsive layout](https://vuestic.epicmax.co/#/admin/dashboard) |
[charts (Chart.js)](https://vuestic.epicmax.co/#/admin/statistics/charts) |
[progress bars](https://vuestic.epicmax.co/#/admin/statistics/progress-bars) |
[forms](https://vuestic.epicmax.co/#/admin/forms/form-elements) |
[selects](https://vuestic.epicmax.co/#/admin/forms/form-elements) |
[date pickers](https://vuestic.epicmax.co/#/admin/forms/form-elements) |
[checkboxes and radios](https://vuestic.epicmax.co/#/admin/forms/form-elements) |
[static tables and data tables](https://vuestic.epicmax.co/#/admin/tables/data) |
[medium editor](https://vuestic.epicmax.co/#/admin/forms/medium-editor) |
[smooth typography](https://vuestic.epicmax.co/#/admin/ui/typography) |
[buttons](https://vuestic.epicmax.co/#/admin/ui/buttons) |
[collapses](https://vuestic.epicmax.co/#/admin/ui/collapses) |
[color pickers](https://vuestic.epicmax.co/#/admin/ui/color-pickers) |
[timelines](https://vuestic.epicmax.co/#/admin/ui/timelines) |
[toasts](https://vuestic.epicmax.co/#/admin/ui/notifications) |
[tooltips](https://vuestic.epicmax.co/#/admin/ui/popovers) |
[popovers](https://vuestic.epicmax.co/#/admin/ui/popovers) |
[icons](https://vuestic.epicmax.co/#/admin/ui/icons/) |
[spinners](https://vuestic.epicmax.co/#/admin/ui/spinners) |
[modals](https://vuestic.epicmax.co/#/admin/ui/modals) |
[file upload](https://vuestic.epicmax.co/#/admin/ui/file-upload) |
[chips](https://vuestic.epicmax.co/#/admin/ui/chips) |
[trees](https://vuestic.epicmax.co/#/admin/ui/tree-view) |
[cards](https://vuestic.epicmax.co/#/admin/ui/cards) |
[ratings](https://vuestic.epicmax.co/#/admin/ui/rating) |
[sliders](https://vuestic.epicmax.co/#/admin/ui/sliders) |
[chat](https://vuestic.epicmax.co/#/admin/ui/chatPage) |
[maps (Google, Yandex, Leaflet, amMap)](https://vuestic.epicmax.co/#/admin/maps/google-maps) |
[login/signup pages templates](https://vuestic.epicmax.co/#/auth/login) |
[404 pages templates](https://vuestic.epicmax.co/#/admin/pages/404-pages) |
[i18n](https://vuestic.epicmax.co/#/admin/dashboard)


## Contributing
Thanks for all your wonderful PRs, issues and ideas. You’re always welcome to [join](https://github.com/epicmaxco/vuestic-admin/blob/master/.github/CONTRIBUTING.md)!

## License
[MIT](https://github.com/epicmaxco/vuestic-admin/blob/master/LICENSE) license.
