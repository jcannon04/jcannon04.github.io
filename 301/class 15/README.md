# Authentication

* **What is OAuth?** OAuth is an open standard for access delegation, commonly used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords.
* **Give an example of what using OAuth would look like.** When you go to log onto a website and it gives you the option to log in with your google account.
* **How does OAuth work? What are the steps that it takes to authenticate the user?** OAuth doesn't share password data but instead uses authorization tokens to prove an identity between consumers and service providers. OAuth is an authentication protocol that allows you to approve one application interacting with another on your behalf without giving away your password.

* **What is OpenID?** OpenID is an open standard and decentralized authentication protocol.
* **What is the difference between authorization and authentication?** Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.
* **What is Authorization Code Flow?** Authorization code flow is a two-step authorization process that uses an authorization code and access token.
* **What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?** PKCE is an extension to the Authorization Code flow to prevent several attacks and to be able to securely perform the OAuth exchange from public clients.
* **What is Implicit Flow with Form Post?** The Implicit Flow with Form Post is an older OAuth flow primarily used for single-page applications (SPAs) where the client-side JavaScript handles the authentication process. It is less secure than the Authorization Code Flow because it directly returns the access token to the client. Here's how it works:
* **What is Client Credentials Flow?** The Client Credentials flow is a server to server flow. There is no user authentication involved in the process. In fact there is no user at all, the resulting access tokens will not contain a user, but will instead contain the Client ID as subject (if not configured otherwise).
* **What is Device Authorization Flow?** The Device Authorization Flow is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token.
* **What is Resource Owner Password Flow?** The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. The primary difference is that the user's password is accessible to the application. This requires strong trust of the application by the user.
