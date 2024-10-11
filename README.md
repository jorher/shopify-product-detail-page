### Install commands
* **NOTE:** before running an install see if you already have a version installed by typing `shopify version` in your terminal *

```
yarn global add @shopify/cli@latest
brew install ruby
```

### Authenticate
This will connect to the shopify stores.  Currently there are two stores that we need to connect to:
`shopify login [--store jhkurk]`

## development
1) Clone the theme repo.  To start the project you will need to run `git clone https://github.com/jorher/shopify-product-detail-page.git`.  Since this is a private repo you will have to use your username to access it.

2) Inside your project folder you will need to run the command `shopify theme dev --store jhkurk`.  This will create a local dev environment for the theme.  Three links will be created: localhost, theme editor and preview.  Any changes you make will be automatically reflected on your links. This is only synced to your system so the only changes you will see will be yours.
store password: pesayn

3) Make your code edits and push your changes.  

## Development notes
- When you push any changes to the theme branch they will be automatically reflected on the staged theme on carnegie-hall. By pushing changes is the only way for the other developers to see what you have done.  
- Code can be changed either locally through your IDE or on the carnegie-hall site by clicking actions>edit code on the theme. Any edits made this way will get an automatic push to the git repo by the shopify bot.  
- You can customize the look of the site and make tweaks to it through the theme customizer. *NOTE* DO NOT use the theme editor link you got when you ran `shopify theme dev --store jhkurk`.  This only edits your local copy. Instead you MUST use the customizer button on the actual theme.

### Basic commands
Both Shopify and GIT commands to use during development.
## GIT
`git pull` - This will pull all the recent changes from the remote repository to your local.  This would be best run on the main branch of the repo.
`git merge <A>` - This allows you to pull changes from one branch onto your current branch.  This needs to be run on your active branch. `<A>` is the name of the branch that you want to bring changes in from.
`git add <FILE>` - Stages changes to your local files to get ready to be pushed.  You will need to either specify the specific file or use a "." to select all files.
`git commit -m "MESSAGE"` - Commits your changes with a message.  This is the final step before you push your changes to the repo.
`git push` - sends your changes locally to the remote repository.

## Shopify
- `Shopify help` - the basic help command to display help and information about commands.
- `shopify login [--store jhkurk]` - logs you into the shopify store.  In this case it will be "jhkurk".
- `shopify theme list` - list all the available themes for the store.
- `shopify theme dev --store jhkurk` - creates a local version of the theme with hot-reload so any changes are display automatically.