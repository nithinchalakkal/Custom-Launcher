# Customized-android-launcher-for-kiosk-application
Library helps you to control the specific application launcher from other android modules using android overlay

Module Description:
Using this library module, Developer can manage the the kiosk application's launcher/Exit programatically .

USAGE :

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
