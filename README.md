# F.A.Q.
#### My build keeps failing because the object id's aren't in range [50000..99999]
add "enablePerTenantExtensionCop": false to .github/AL-Go-Settings

#### Adding a depenency to another repo
```
"appDependencyProbingPaths":  [
        {
            "repo": "https://github.com/<organization>/<repository>",
            "version": "latest",
            "release_status": "release",
            "authTokenSecret": "GHTOKENWORKFLOW"
        }
```
#### Github won't stop asking me to sign in (from VSCode)
git remote set-url origin https://dvanes67@github.com/<organization>/<repo>.git
and it will.

#### Getting a QA (sandbox) secret
New-BcAuthContext -includeDeviceLogin | New-ALGoAuthContext | Set-Clipboard
create QA_AUTHCONTEXT secret and paste.
