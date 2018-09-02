# NeedfulThings
A list of commands and notes I have found useful 

### Unset Global Proxies
git config --global --unset https.proxy

### Clean local git branches that aren’t part of remote  - change dev to master if you need to 
git branch --merged dev | grep -v '^[ *]*dev$' | xargs git branch -d

### Open Chrome unsecured 
 open -na "Google Chrome" --args --disable-web-security --user-data-dir="/tmp/chrome-dev-session"
 
### key gen and copy to clipboard 
ssh-keygen -t rsa

pbcopy < ~/.ssh/id_rsa.pub

## Use npm commands
npm help-search 

npm list --depth 0 --long true
