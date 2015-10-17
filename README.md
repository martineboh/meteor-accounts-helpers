This package provides helpful helpers to deal with users.

Installation
------------

``` sh
meteor add gwendall:accounts-helpers
```

## Server methods  

***Accounts.onJoin(cb({ user: ..., provider: ... }))***: On user joins for the first time [1].
***Accounts.disconnect(userId, provider)***: Disconnect a social account.  

[1]: onJoin does not trigger when Accounts.createUser is called with no client/user intent.

## Client methods  

***Accounts.onLogin(cb)***: Hook for user log in.  
***Accounts.onLogout(cb)***: Hook for user log out.  
***Accounts.onConnect(cb(provider))***: Hook for user connecting a social account when already logged in.    
***Accounts.onDisconnect(cb(provider))***: Hook for user disconnecting a social account when already logged in.    
***Accounts.disconnect(provider, cb)***: Disconnect a social account.  

## Client template helpers  

***<span data-accounts-loginwith={{provider}}>Login with {{provider}}</span>***: Logs in the user with a given provider.  
***<span data-accounts-disconnect={{provider}}>Disconnect {{provider}}</span>***: Removed the given provider's credentials from the user.  
***<span data-accounts-logout>Log out</span>***: Logs the user out.
