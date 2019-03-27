# Customized-android-launcher-for-kiosk-application
Library helps you to control the specific application launcher from other android modules using android overlay

Module Description:
Using this library module, Developer can manage the the kiosk application's launcher/Exit programatically .

USAGE :
================

How to Include an External .aar File Using Gradle?
================

Step 1. File -> New -> New Module -> Import .jar/.aar and import your .aar.

Step 2. Then in your project’s build.gradle (the one under ‘app’) add the following:

Step 3:
dependencies {
 compile project(‘:Name-of-the-Project’)
}

Step 4:
Clean Build after all the above steps


Where you want to load the launcher
========================================
				Bundle extras = new Bundle();
				extras.putString("Packagename", getPackageName());
				Intent i = new Intent(this, FloatingLauncher.class);
				i.putExtras(extras);
				startActivity(i);
				finish();



Where you want to Stop the launcher || Normally  in OnStart()
========================================
				
				stopService(new Intent(this, FloatingViewService.class));
