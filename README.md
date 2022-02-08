# ACD

```
005-02-acd
```

## Create a store using shopify partner
## Install shopify CLI

## Check shopify CLI version

```
shopify version
gem update shopify-cli
```

## Initialize a new theme using Dawn

```
shopify theme init
  ? Theme name: 005-02-acd
```

## Authenticate with Shopify CLI

```
shopify login --store 005-02-acd.myshopify.com
```

## Preview your theme

```
shopify theme serve
  Error
    You are not authorized to edit themes on 005-02-acd.myshopify.com.
```

## If error use this method

```
shopify logout

web browser
  shopify
    copy password under protection password
    logout
  https://005-02-acd.myshopify.com
    password: input password from protection password

shopify login --store 005-02-acd.myshopify.com
  web browser
    Authenticated successfully. You may now close this page.
```

## Preview your theme

```
shopify theme serve

web browser
  http://127.0.0.1:9292                                                     = local
  https://005-02-acd.myshopify.com/admin/themes/130728001779/editor         = Online Store Editor
  https://005-02-acd.myshopify.com/?preview_theme_id=130728001779           = Share preview link
```

## Create Github repository

```
new repository
  repository name: 005-02-acd
  public
  create repository

git branch -M main                                                     copy this 3 gitcommands from github
git remote add origin git@github.com:angelocdz/005-02-acd.git
git push -u origin main
```

## Create Git repository

```
git init
git status
git add .
git commit -m 'Git initialize'
git log --oneline

Input the git commands from github.

web browser
  refresh repository
  https://github.com/angelocdz/005-02-acd
```

## Install the Shopify GitHub integration and connect your branch to your store

```
https://005-02-acd.myshopify.com/admin
  online store, themes, add theme, connect from github
    select, 005-02-acd, connect, click x icon
      005-02-acd/main
```

## Test shopify githubt integration

```
vi config/settings_schema.json
  "theme_name": "005-02-acd"

git status
git add .
git commit -m 'Test shopify github integration & updated Theme Name to 005-02-acd'
git push -u origin main

web browser
  Check github if push is successful.
  https://005-02-acd.myshopify.com/admin
    online store, themes
      005-02-acd/main
        customize
          Click the 3 dots then it will display.
            005-02-acd
Successfully integrated github to our shopify store.
```

## Publish your theme

```
shopify
  online store, themes
    005-02-acd/main, actions, publish, publish

Successfully published the 005-02-acd theme now it's on production or live.
```
