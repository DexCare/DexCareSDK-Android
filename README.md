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
		url "https://maven.pkg.github.com/DexCare/DexCareSDK-Android/"
	}
}
```

Also add the following implementation to the dependencies section of your app's build.gradle file:
```
dependencies {
	implementation "org.dexcare:dexcare:4.0.3"
}
```
