# DexCareSDK-Android


To install, add the following to your project root's build.gradle file, and replace `githubUserName` and `githubToken` with your credentials used to access this repository:
```
repositories {
	maven {
		url "https://maven.pkg.github.com/Health-V2-Consortium/DexCareSDK-Android/"
		credentials {
			username "githubUserName"
			password "githubToken"
		}
	}
}
```

Also add the following implementation to the dependencies section of your app's build.gradle file:
```
dependencies {
	implementation "org.dexcare:dexcare:2.2.0"
}
```
___
If you don't want to hardcode the credentials, they can be set as environment variables and then accessed in the build.gradle file like so:

```
repositories {
	maven {
		url "https://maven.pkg.github.com/Health-V2-Consortium/DexCareSDK-Android/"
		credentials {
                	username System.getenv("DEXCARE_MAVEN_ACCOUNT")
                	password System.getenv("DEXCARE_MAVEN_TOKEN")
		}
	}
}
```
