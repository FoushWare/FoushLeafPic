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




