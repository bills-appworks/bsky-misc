In Bluesky, the authentication method for Bluesky accounts (users), including unofficial apps, is scheduled to change from **"App Password"** to **"OAuth"** in the future. As of January 2026, both methods coexist, and the discontinuation of App Password is being considered for the future.

> Reference: <a href="https://docs.bsky.app/blog/oauth-atproto" target="bsky">OAuth for AT Protocol (one of Bluesky's official announcements)</a>

"Authentication" is the process of proving your identity, such as by entering a password. You may have seen it in terms like "login" or "sign in".

Some apps and web services (hereinafter collectively referred to as "apps") use OAuth instead of App Password for authentication. However, some people may feel uneasy because a confirmation of the permissions to be granted to the app is displayed on the authentication screen.

<div align="center">

<img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreih3qsj5lv23ghhaq5bjuzukbtsfk3nqxzfjgbpy45wkrfvgfat3ny" width="600">

<font color="gray">Example of a permission confirmation screen</font>

</div>

However, OAuth is used in apps around the world as a more secure authentication method than app-specific passwords. When using some apps, you may often see authentication options like "Login with \*\*\*" (where \*\*\* is a service that manages accounts, such as Google), instead of the app's own password. These use the same OAuth mechanism.


<div align="center">

| <img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreicpxuq4labvr72bovur25sg6wzop444pyrcg66g4t5znnf42a4kz4" width="220"> | <img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreie7ry7f7rjixezuhbverlej77oldys62jkjjz4ba2exkysmsi4yxa"> |<img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreide7eusud5ba3phfz6gdjcynw3yue6mm632nwbvncpx4rpmz6fbbm">
| --- | --- | --- |

<font color="gray">Examples of buttons for authenticating with OAuth</font>

</div>

The following is an overview of the differences between OAuth and App Password in Bluesky.

|Comparison|App Password|OAuth|
| --- | --- | --- |
| Permissions granted to the app | You can choose whether to grant permission for chat (DM). Otherwise, **many things are possible**. | **Limited** to the permissions displayed on the authentication screen. |
| Password input | **Referenced by the app** for proxy authentication with Bluesky. | **Not referenced by the app**. Authentication is done by **entering the password on the Bluesky screen** after navigating, and only a temporary random key for the scope of permissions is passed to the app. |
| Disabling App Password | Possible | - (App Password do not exist) |

On the OAuth authentication screen, the permissions granted to the app are displayed, which may make some users anxious about whether they are granting more permissions than necessary. However, with App Password, it's just not displayed; except for the choice of whether to grant permission for chat (DM), it grants a wide range of permissions for operations possible with the account. OAuth presents the limited permissions as a matter of accountability so that users can make an informed decision.

Also, regarding password input, as you can see by looking at the address bar (URL field) in your web browser, the domain is Bluesky's (such as `bsky.social`), not the app's itself. This shows that the password itself is processed by Bluesky without the app's involvement.


<div align="center">

<img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreiabvclgohkdatjb5nlwdresqgmqurerwoarur63kwe5mok6m7bmee" width="600">

<font color="gray">Example of an OAuth authentication screen (the domain in the address bar at the top is the official Bluesky bsky.social)</font>

</div>

<div align="center">

<img src="https://verpa.us-west.host.bsky.network/xrpc/com.atproto.sync.getBlob?did=did%3Aplc%3Alfjssqqi6somnb7vhup2jm5w&cid=bafkreia2o3fd7ieblts7qkrn3lgox27u7gqhgftuyzjerwjgytoi766lsm" width="600">

<font color="gray">Simplified flow of OAuth authentication</font>

</div>

Regarding the displayed permissions, the options currently available from apps provided by Bluesky are broad, so they may not seem to match the app's functional scope. This is being continuously improved to allow for more granular permission scopes, so it is expected that the scope of permissions will be more limited in the future.

Of course, just because it's OAuth doesn't mean it's absolutely safe. The app can perform operations on the account within the scope of the permissions granted by Bluesky, so whether you can trust the app itself is your own judgment, just as with App Password.

However, as mentioned above, OAuth is not more dangerous or less trustworthy than App Password, so please use it without anxiety!

It is also possible to check and revoke apps that have been authenticated with OAuth. For details, please refer to the following article by **anon** [@anon5r.com](https://bsky.app/profile/did:plc:c22jdrqhoajyj5ca7e56a3ke).

(This is a Japanese article.)
[BlueskyでOAuth認証したアプリの管理について (About managing apps authenticated with OAuth on Bluesky)](https://whtwnd.com/anon5r.com/3mb7a3swfrq2v)

[Added on 2026/1/21]

For more information on the background of why some apps use App Passwords and others use OAuth, the following article by **anon** [@anon5r.com](https://bsky.app/profile/did:plc:c22jdrqhoajyj5ca7e56a3ke) is helpful.

(This is a Japanese article.)
[AppPasswordとOAuthについておさらい @anon5r.com (A review of AppPassword and OAuth @anon5r.com)](https://whtwnd.com/anon5r.com/3mchzlxdo222p)
