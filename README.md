# React GitHub Login

![NPM](https://img.shields.io/npm/v/github-login.svg?style=flat)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/1cc6efd5d9174487b35296df925885ad)](https://app.codacy.com/app/donmorton/github-login?utm_source=github.com&utm_medium=referral&utm_content=donmorton/github-login&utm_campaign=Badge_Grade_Dashboard)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdonmorton%2Fgithub-login.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdonmorton%2Fgithub-login?ref=badge_shield)

React component for [GitHub login](https://developer.github.com/v3/oauth/).

This project originally created and maintained by [Checkr](https://www.npmjs.com/package/react-github-login). However, after over a year of inactivity it appears this repository is abandoned. With many issues open, I decided to clone and maintain this repo myself. 

Credit goes to [Kurt Ruppel](https://github.com/kruppel) from Checkr for being the original developer on the project. 

This project is now being updated and maintained by [donmorton](https://github.com/donmorton)

## Usage

```js
import React from 'react';
import ReactDOM from 'react-dom';
import GitHubLogin from 'github-login';

const onSuccess = response => console.log(response);
const onFailure = response => console.error(response);

ReactDOM.render(
  <GitHubLogin clientId="ac56fad434a3a3c1561e"
    onSuccess={onSuccess}
    onFailure={onFailure}/>,
  document.getElementById('example')
);
```

### Props

#### `clientId`

`{string}` _required_

Client ID for GitHub OAuth application.

#### `redirectUri`

`{string}`

Registered redirect URI for GitHub OAuth application.

#### `scope`

`{string}`

Scope for GitHub OAuth application. Defaults to `user:email`.

#### `className`

`{string}`

CSS class for the login button.

#### `buttonText`

`{string}`

Text content for the login button.

#### `onRequest`

`{function}`

Callback for every request.

#### `onSuccess`

`{function}`

Callback for successful login. An object will be passed as an argument to the callback, e.g. `{ "code": "..." }`.

#### `onFailure`

`{function}`

Callback for errors raised during login.


## Development

```sh
$ npm start
```

Webpack development server starts at [http://localhost:8080](http://localhost:8080), loading [example/index.html](github.com/checkr/react-facebook-login/tree/master/example/index.html).


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdonmorton%2Fgithub-login.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdonmorton%2Fgithub-login?ref=badge_large)