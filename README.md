# DexCareSDK-Android

See https://developers.dexcarehealth.com/ for documentation and a migration guide.

To install, add the following to your project root's build.gradle file, and replace `githubUserName` and `githubToken` with your credentials used to access this repository:
```
repositories {
        // required for rxpermissions (DexCare SDK dependency)
        maven { url "https://jitpack.io" }

        // required for tokbox (DexCare SDK dependency)
        maven { url 'https://tokbox.bintray.com/maven' }
	maven {
		url "https://maven.pkg.github.com/DexCare/DexCareSDK-Android/"
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
	implementation "org.dexcare:dexcare:4.0.3"
}
```
___
If you don't want to hardcode the credentials, they can be set as environment variables and then accessed in the build.gradle file like so:

```
repositories {
        // required for rxpermissions (DexCare SDK dependency)
        maven { url "https://jitpack.io" }

        // required for tokbox (DexCare SDK dependency)
        maven { url 'https://tokbox.bintray.com/maven' }
	maven {
		url "https://maven.pkg.github.com/DexCare/DexCareSDK-Android/"
		credentials {
                	username System.getenv("DEXCARE_MAVEN_ACCOUNT")
                	password System.getenv("DEXCARE_MAVEN_TOKEN")
		}
	}
}
```
