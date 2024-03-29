## Getting Lenovo Laptop WIFI working with linux 

 * sudo add-apt-repository -r ppa:kelebek333/kablosuz 
 * sudo apt purge rtw89-dkms 
 * sudo apt update
 * sudo apt install git bc
 * git clone https://github.com/HRex39/rtl8852be.git
 * cd rtl8852be
 * make
Several possibly harmless warnings will appear.

* sudo make install
Reboot. You will probably need to disable secure boot.

After each kernel update, you must recompile:

* cd rtl8852be
* make clean
* git pull
* make
* sudo make install

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

When using python use pyenv to manage different versions of python like nvm or n for javascript.

#### Uninstall minikube from System
minikube stop; minikube delete &&

docker stop $(docker ps -aq) &&

rm -rf ~/.kube ~/.minikube &&

sudo rm -rf /usr/local/bin/localkube /usr/local/bin/minikube &&

launchctl stop '*kubelet*.mount' &&

launchctl stop localkube.service &&

launchctl disable localkube.service &&

sudo rm -rf /etc/kubernetes/ &&

docker system prune -af --volumes

#### SPCTL

sudo spctl --master-disable //enables the ability to Allow 3rd party developer tools in Security and Privacy -> Allow

#### Running Kafka environments
# Start the ZooKeeper service
# Note: Soon, ZooKeeper will no longer be required by Apache Kafka.
$ bin/zookeeper-server-start.sh config/zookeeper.properties

# Start the Kafka broker service
$ bin/kafka-server-start.sh config/server.properties
