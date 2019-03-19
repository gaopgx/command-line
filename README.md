# command-line
## expectation usage
#### see-dashboaed

original usage
 ```
 python ./src/git-analyzer.py --action clone \
--basepath [Project Path]
--token xxxxxxxxxx --group_id 2070

 python ./src/git-analyzer.py --action create_pipelines \
--basepath [Project Path]
--token xxxxxxxxxx --group_id 2070


python ./src/git-analyzer.py --action create_pipelines_by_file \
--metadata_path "[Project Metadata Path ]"
 
 ```
 expectation usage
  ```
  dashboard clone --basepath [Project Path] --token xxxxxxxxxx --group_id 2070
  
  dashboard create --basepath [Project Path] --token xxxxxxxxxx --group_id 2070
  
  dashboard create_file --basepath [Project Path] --token xxxxxxxxxx --group_id 2070
  
  ```
 
 #### see-code-standard
 
 original usage
  ```
# check java project
python ./src/see.py --action checkstyle --basepath ~/daimler-git/china/its/cd/otr/account-management --language java --ignoredir use,comma,split,your,path,exclude
# check javascript react-native project
python ./src/see.py --basepath ~/daimler-git/china/its/cd/otr/dms-helper-frontend --language js --platform react-native --action checkstyle --ignoredir test,tests,target,build,dist,node_modules,i18n,metronic*,dwz*,Microsoft*.js,jquery*,jquery*.js,*.min.js,*-min.js,assets,dms-helper,swagger,miniui,angular*,SiteAssets/JS/sp.js,sp*.js,FrogTMS/FrogTMS.WebUI/obj,layui,Plugins,*spec.js
# check javascript project
python ./src/see.py --basepath ~/daimler-git/china/its/cd/otr/dms-helper-frontend --language js --action checkstyle --ignoredir test,tests,target,build,dist,node_modules,i18n,metronic*,dwz*,Microsoft*.js,jquery*,jquery*.js,*.min.js,*-min.js,assets,dms-helper,swagger,miniui,angular*,SiteAssets/JS/sp.js,sp*.js,FrogTMS/FrogTMS.WebUI/obj,layui,Plugins,*spec.js
# check typescript project
python3 ./src/see.py --action checkstyle --basepath ~/daimler-git/china/its/cd/otr/website/src/**/*.ts --language typescript

  
 ```
 expectation usage
 ```
 checkstyle --basepath ~/daimler-git/china/its/cd/otr/account-management --language java --ignoredir use,comma,split,your,path,exclude
 
 
 
 ```
 



#### checkstyle [options] [file|dir]

The command line utility has several options. You can view the options by running 
checkstyle -h
checkstyle [-h][-basepath BASEPATH][-language LANGUAGE]

Sample of usage ::

checkstyle -basepath maven/com.daimler/BBAC -language java

checkstyle -basepath ../meclub_web -language js -ignoredir test,tests,target,build,dist,node_modules,i18n,metronic*,dwz*,Microsoft*.js,jquery*,jquery*.js,*.min.js,*-min.js,assets,dms-helper,swagger,miniui,angular*,SiteAssets/JS/sp.js,sp*.js,FrogTMS/FrogTMS.WebUI/obj,layui,Plugins,*spec.js

Example of checkstyle output

![example](https://github.com/gaopgx/command-line/blob/master/example-of-checkstyle-output.PNG?raw=true)

#### optional arguments

 * -h, -help            show this help message and exit
 * -action ACTION       action
 * -notified            notify when job failed
 * -language LANGUAGE   language
 * -platform PLATFORM   platform like: react, react-native etc
 * -basepath BASEPATH   basepath of code repo
 * -ignoredir IGNOREDIR ignore dir 
 
## Reference

see[#1](https://eslint.org/docs/user-guide/command-line-interface)
see[#2](http://pylint.pycqa.org/en/stable/user_guide/run.html)

## original usage 

python3 ./src/see.py --action checkstyle --basepath ../meclub_web --language js --ignoredir test,tests,target,build,dist,node_modules,i18n,metronic*,dwz*,Microsoft*.js,jquery*,jquery*.js,*.min.js,*-min.js,assets,dms-helper,swagger,miniui,angular*,SiteAssets/JS/sp.js,sp*.js,FrogTMS/FrogTMS.WebUI/obj,layui,Plugins,*spec.js
