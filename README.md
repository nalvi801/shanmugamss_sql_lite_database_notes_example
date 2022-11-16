*shanmugam*

I downloaded this github from extenal repo.

Source Repo : https://github.com/JohannesMilke/sqflite_database_example.git

I have made the following changes to solve version errors.




****---------------------------------------   android/app/build.gradle --------------------------------------------------------
android/app/build.gradle       —>  ( 2 places to change )

android {
   compileSdkVersion 31 


defaultConfig {
   applicationId "com.example.sqflite_database_example"
   minSdkVersion 30
   targetSdkVersion 30
   versionCode flutterVersionCode.toInteger()
   versionName flutterVersionName
}

****---------------------------------------------------android/build.gradle ----------------------------------------------

android/build.gradle  ( —-> Change in 2 places )

buildscript {
   ext.kotlin_version = '1.7.0'


dependencies {
   classpath 'com.android.tools.build:gradle:7.1.2'
   classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
}



****----------------------------------------- \android\gradle\wrapper\gradle-wrapper.properties ------------------------------------------------------------------------------

Gradle-wrapper.properties  ( Path   \android\gradle\wrapper\gradle-wrapper.properties

#Fri Jun 23 08:50:38 CEST 2017
distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists
distributionUrl=https\://services.gradle.org/distributions/gradle-7.4-all.zip



