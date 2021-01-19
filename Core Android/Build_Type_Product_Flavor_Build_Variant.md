- Build type
	- Build type controls how to build packages of your app.

	- the build system defines two build types `debug` and `release`.
	```
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
        debug{
        	applicationIdSuffix ".debug"
        }
        /**
         *The `initWith` property allows to copy configurations from other build types.
         *This copies the debug build type and changes the manifestplaceholder and applicationIdSuffix
         */
        staging{
        	initWith debug
        	manifestPlaceHolders = [hostName:"internal.example.com"]
        	applicationIdSuffix ".debugStaging"
        }
    }
	```
- Product Flavours
	- Product flovours provide a customized version of the application build.

	- It is used to define custom features , minimum and target API levels.

	- This can help create different labeled apps as well.

	```
	flavourDimensions "version"
	productFlovours {
		demo {
			dimension "version"
			applicationIdSuffix ".demo"
			versionNameSuffix "-demo"
		}
		full {
			dimension "version"
			applicationIdSuffix ".full"
			versionNameSuffix "-full"
		}
	}
	```
- Build varient 
	- The Combination of Build types and product flavours is known as Build Varient.

	- For the above build types (debug and release) and product flavour (demo and full version), build varient can be `demoDebug`,`demoRelease`,`fullDebug` and `fullRelease`.