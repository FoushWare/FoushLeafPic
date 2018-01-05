### Search for every part that i'm reading ...

##### `>> Manifest`
  * `Activity Tag`
    *             android:configChanges="orientation|screenSize"
    
    Description
* The idea is to handle orientation, screenSize and keyboard appearance/disappearance changes by implement onConfigurationChanged in the Activity java code 
    * example for using that 
        * Hide fab button in portrate layout
        * Make the keyboard appear
* You can see that in MainActivity 
~~~~
  @Override
public void onConfigurationChanged(Configuration newConfig) {
     super.onConfigurationChanged(newConfig);
    if (newConfig.orientation != Configuration.ORIENTATION_LANDSCAPE) {
            fab.setVisibility(View.VISIBLE);
            fab.animate().translationY(fab.getHeight() * 2).start();
        } else
            fab.setVisibility(View.GONE);
    }
~~~~
        


   [more reading ...](http://code.hootsuite.com/orientation-changes-on-android/)             
* `Actions /Main...`
    *             android.intent.action.MAIN"
 Description
* means that this activity is the entry point of the application, i.e. when you launch the application, this activity is created.
* `Actions /GET_CONTENT...`

    * Code
~~~~
     <intent-filter android:label="@string/app_name">
             <action android:name="android.intent.action.GET_CONTENT" />
                <data android:mimeType="image/*" />
                <data android:mimeType="video/*" />
     </intent-filter>
 ~~~~
 Description
* Just as your application can send data to other applications, so too can it easily receive data from applications , and `data tage` specify the type of data to get from other applications

### Usage in code Java

~~~~~
pickMode = getIntent().getAction().equals(Intent.ACTION_GET_CONTENT) || getIntent().getAction().equals(Intent.ACTION_PICK);

Intent intent = new Intent(SplashScreen.this, MainActivity.class);

  if (pickMode) {
            intent.putExtra(SplashScreen.PICK_MODE, pickMode);
            startActivityForResult(intent, PICK_MEDIA_REQUEST);
    } else {
            startActivity(intent);
            finish();
        }
~~~~~






   [more reading ...](https://developer.android.com/training/sharing/receive.html)

* `Category ...` 

    *             android:name="android.intent.category.DEFAULT"
 Description
* This is related to the Android operating system The os assign some Categories so every application know them ,this is useful if we running for example :launcher and the launcher want to show the apps for Google and list them in group ,it will start searching in all app's Manifest for category called Google then list them


   [more reading ...](https://stackoverflow.com/questions/6782820/what-does-category-in-the-manifest-mean)
   
## `APP UI`
* The app uses 
    *  ` CardView with RecyclerView` 
        * i've made implementation of this Here [FoushCardView](https://github.com/AhmedFouad60/FoushCardView)
        * [Tutorial](https://www.learn2crack.com/2016/02/android-recyclerview-and-cardview.html)










   
   
 



