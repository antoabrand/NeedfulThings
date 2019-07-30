## Git

#### Merge a single file 
git checkout branch path/to/file

#### Unset Global Proxies
git config --global --unset https.proxy

#### Clean local git branches that aren’t part of remote  - change dev to master if you need to 
git branch --merged dev | grep -v '^[ *]*dev$' | xargs git branch -d

## Open Chrome unsecured 
 open -na "Google Chrome" --args --disable-web-security --user-data-dir="/tmp/chrome-dev-session"
 
## Key gen and copy to clipboard 

#### For Mac
ssh-keygen -t rsa

pbcopy < ~/.ssh/id_rsa.pub

#### For Windows

(under construction)

## npm commands
npm help-search 

npm list --depth 0 --long true

## Flow 

FLOW-TYPED

flow-typed install package@version

flow-typed create-stub package@version

## Prettier
scripts:{
 "pretty": "prettier --write --tab-width 2 \"src/**/*.ts\"",
 "precommit": "lint-staged"
  },
  "lint-staged": {
    "*.ts": [
      "npm run pretty",
      "git add"
    ]
  },

## MAC

#### SPCTL

sudo spctl --master-disable
