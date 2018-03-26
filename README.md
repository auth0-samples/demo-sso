# Auth0 SSO Demo

This sample demonstrates how to configure your Universal Login Page to automatically sign in if you have an SSO session without passing prompt=none

## Getting Started

If you haven't already done so, [sign up](https://auth0.com) for your free Auth0 account and create a new client in the [dashboard](https://manage.auth0.com).
* Find the **domain** and **client ID** from the settings area and add the URL for your application to the **Allowed Callback URLs** box.
* If you are serving the application with the provided `serve` library, you will need to add '127.0.0.1 test.local' to your hosts file and then the URL for allowedCallbacks is `http://test.local:3000`.
* Add 'http://test.local:3000' to your Allowed Logout URLs in your tenant settings (upper right drop down menu->Settings->Advanced)*[]:
* Clone this repo.

```bash
cd demoSSO
yarn install
```

## Set the Client ID and Domain

Rename the `auth0-variables.sample.js` file to `auth0-variables.js` and provide the **client ID** and **domain** there.

## Initialize your Universal Login Page

* Log into manage.auth0.com
* Click Hosted Pages
* Make sure that "Customize Login Page" is turned on
* Copy the contents of universalLoginPage.html to the code box
* Click Save

## Run the Application

The `serve` module provided with this sample can be run with the `start` command.

```bash
yarn run start
```

The application will be served at `http://test.local:3000`.

## How to Test that SSO is working

Logging in the first time should create your SSO session.
When you are returned to the page, click "Kill Session", this will remove your application browser session, but not your Auth0 SSO session.  Refreshing the page should leave you logged out, but if you click Login, you should automatically log in without having to enter credentials.
When you click "Logout" it will kill your SSO session, clicking login should prompt you to enter your credentials.

## What is Auth0?

Auth0 helps you to:

* Add authentication with [multiple authentication sources](https://docs.auth0.com/identityproviders), either social like **Google, Facebook, Microsoft Account, LinkedIn, GitHub, Twitter, Box, Salesforce, amont others**, or enterprise identity systems like **Windows Azure AD, Google Apps, Active Directory, ADFS or any SAML Identity Provider**.
* Add authentication through more traditional **[username/password databases](https://docs.auth0.com/mysql-connection-tutorial)**.
* Add support for **[linking different user accounts](https://docs.auth0.com/link-accounts)** with the same user.
* Support for generating signed [Json Web Tokens](https://docs.auth0.com/jwt) to call your APIs and **flow the user identity** securely.
* Analytics of how, when and where users are logging in.
* Pull data from other sources and add it to the user profile, through [JavaScript rules](https://docs.auth0.com/rules).

## Create a free Auth0 account

1. Go to [Auth0](https://auth0.com/signup) and click Sign Up.
2. Use Google, GitHub or Microsoft Account to login.

## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section. Please do not report security vulnerabilities on the public GitHub issue tracker. The [Responsible Disclosure Program](https://auth0.com/whitehat) details the procedure for disclosing security issues.

## Author

[Auth0](https://auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE.txt) file for more info.



