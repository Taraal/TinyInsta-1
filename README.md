# webandcloud

**Be sure your maven has access to the web**
* you should have file ~/.m2/settings.xml
* otherwise cp ~molli-p/.m2/settings.xml ~/.m2/

```
molli-p@remote:~/.m2$ cat settings.xml
<settings>
 <proxies>
 <proxy>
      <active>true</active>
      <protocol>https</protocol>
      <host>proxy.ensinfo.sciences.univ-nantes.prive</host>
      <port>3128</port>
    </proxy>
  </proxies>
</settings>
```

## import and run in eclipse
* install the code in your home:
```
 cd ~
 git clone https://github.com/momo54/webandcloud.git
 cd webandcloud/myapp2018
 mvn install
```
* start an eclipse with gcloud plugin
```
 /media/Enseignant/eclipse/eclipse
 or ~molli-p/eclipse/eclipse
 ```
* import the maven project in eclipse
 * File/import/maven/existing maven project
 * browse to ~/webandcloud/myapp2018
 * select pom.xml
 * Finish and wait
 * Ready to deploy and run...
 ```
 gcloud app create error...
 ```
 Go to google cloud shell console (icon near your head in google console)
 ```
 gcloud app create
 ```

## Running from the command line with GCloud SDK
*    Add gcloud in your path:
 *       run /media/Enseignant/google-cloud-sdk/install.sh
*    gcloud config set account yourname
*    gcloud auth login
*    gcloud config set project yourproject

## Install and Run
* git clone https://github.com/momo54/webandcloud.git
* cd webandcloud/myapp2018/
* mvn appengine:deploy
* gcloud app browse


# Access REST API

https://yourapp.appstpot.com/_ah/api/explorer
