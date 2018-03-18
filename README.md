# Example Custom Backend for NetlifyCMS

***Note:*** This is a backend library for NetlifyCMS proposed for GitLab

To use:

Checkout and load dependencies

To load dependencies for build

```bash
yarn
```

To build `dist/fs-backend.js`

```bash
yarn build
```

## How to register with CMS

  - Copy the `dist/gitlab-backend.js` script bundle file into your cms location.
  - Change the `index.html` page to use the backend as in the example below
  - Register the backend Class to the CMS as shown below
  - Change the `config.yml` backend to `backend: gitlab-backend` or the name you registered
  - [Webpack] Add devServer middleware to expose the `/api` path for the file-system API
  - [Stand Alone Server] Create an express server (coming soon) to host the `/api` endpoint

### Add script and register in your CMS page

```html
<head>
  ...
  <script type="text/javascript" src="gitlab-backend.js"/>
</head>
<body>
  <script type="text/javascript" src='cms.js'/>
  <script>
    CMS.registerBackend("gitlab-backend", GitLabBackendClass)
  </script>
</body>
```

## Dependencies

A React Component is required for the auth page of a backend in the NetlifyCMS, so you will need to use React to create the auth page of your backend library.

This library is using some styling that was in the NetlifyCMS, but it is better practice to style the component in your backend auth so a change does not break your component. (hey, call me lazy today 😁)

***WARNING:*** This is a proof of concept at this time, there could be breaking changes to this library. [Alpha Status]

Don't forget: code like you are on 🔥

The Netlify Logo is Copyright of [Netlify][Netlify] and should not be used without their consent.

[Netlify]: https://www.netlify.com/
