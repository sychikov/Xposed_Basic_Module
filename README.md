# Xposed_Basic_Module
Base for Xposed framework workflow with the simple check if it works correct. I've got tired to make new for every module I need.

# Usage
1) Clone this thing on your machine and open like AndroidStudio project.
2) Have fun with developing your own module and god bless you.

# How is it was made?
1) Add your repos into the `build.gradle` after `dependencies` word like that:
```
    compileOnly 'de.robv.android.xposed:api:82'
    compileOnly 'de.robv.android.xposed:api:82:sources'
```
Important moment - use `build.gradle` for module, not for project.

2) Add in `setting.gradle` some kind of that:
```
dependencyResolutionManagement {  
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)  
    repositories {  
        google()  
        mavenCentral()  
        jcenter()  
        maven { url 'https://api.xposed.info/' }  
    }}
```
Try to build it. Don't be sad if it didn't work, you know where you are going.

3) Add in the `AndroidManifest.xml` between <application> tag those things:
```
<meta-data  
    android:name="xposedmodule"  
    android:value="true"/>  
<meta-data  
    android:name="xposeddescription"  
    android:value="Ahahahahahahahahahahahahahahahahah" />  
<meta-data  
    android:name="xposedminversion"  
    android:value="82"/>
```
Try to build it againi. If didn't worked, you can try to cry or sacrifice the lamb. And try from the first step.

4) Make the `assets` folder if you don't have it and put simple file with the name `xposed_init` and path to your main java class like this:
```
com.example.brandnewapplication.Actions
```

5) Build it. Don't worry if AndroidStudio will say that you can't resolve any functions or classes for xposed, it's fine. Just make apk and try to use it.
6) Good luck, bro, you'll need it.
