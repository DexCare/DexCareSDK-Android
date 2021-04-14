# DexCareSDK-Android

See https://developers.dexcarehealth.com/ for documentation and a migration guide.

To install, add the following to your project root's build.gradle file:
```
repositories {
        // required for rxpermissions (DexCare SDK dependency)
        maven { url "https://jitpack.io" }

        // required for tokbox (DexCare SDK dependency)
        maven { url 'https://tokbox.bintray.com/maven' }
	maven {
	
            credentials {
                // You need to be authenticated in order to access the DexCare SDK binaries.
                // Even though they are public, GitHub still requires authentication.
                // Set up the environment variables below with your GitHub credentials.
                username System.getenv("DEXCARE_MAVEN_ACCOUNT") // GitHub email
                password System.getenv("DEXCARE_MAVEN_TOKEN") // GitHub access token
            }
	    url "https://maven.pkg.github.com/DexCare/DexCareSDK-Android/"
	}
}
```

You will need to set up two environment variables `DEXCARE_MAVEN_ACCOUNT` and `DEXCARE_MAVEN_TOKEN`.  These should contain your username & password/access token used to authenticate with GitHub.  Any GitHub account should work.

Also add the following implementation to the dependencies section of your app's build.gradle file:
```
dependencies {
	implementation "org.dexcare:dexcare:6.0.1"
}
```
