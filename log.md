# 100 Days Of Code - Log

### Day 0: January 14, 2017

**Today's Goal:** Begin working on BroadCastReceiver to update RecyclerView when a page is updated.

**Thoughts:** I haven't worked with BroadCast Receivers in a long time. Had to get reacquainted by reading some documentation. 

**Today's Progress:** Restructured app to contain lists of pages in one central class implemented with Singleton pattern. BroadcastReceiver still needs to be completed.

**Next Day's Goal(s)** Finish building BroadcastReceiver and begin implementing JSOUP library

**Link to work:** [Updated App](https://github.com/jgarcia162/Updated)

### Day 1: January 15, 2017

**Today's Goal:**  Finish building BroadcastReceiver and begin implementing JSOUP library

**Today's Progress:** Finished BroadcastReceiver. Found broken logic for checking if a page is updated or not. 

**Next Day's Goal(s)** Fix page updater logic. Implement JSOUP library

**Link to work:** [Updated App](https://github.com/jgarcia162/Updated)

### Day 2: January 28, 2017

**Today's Goal:**  Fix CalledFromWrongThreadException error.

**Today's Progress:** Error fixed. Found some structural issues that need to be addressed. Adapter's data set is being updated on detected update but current method is prone to memory leakage. Need to find an alternate way of updating UI. 

**Next Day's Goal(s)** Find another way to update UI from NotificationService and rearrange UpdateBroadcastReceiver.UpdateCallback

**Link to work:** [Updated App](https://github.com/jgarcia162/Updated/commit/c05d01550c2b7de5637a67281f7d0380006167a6)

### Day 3: February 1, 2017

**Today's Goal:**  Update UI from NotificationService without holding reference to activity and restructure UpdateCallback.

**Today's Progress:** I'm now using a Handler to access the UI thread from NotificationService. Prior use of a reference to the main activity was a memory leak waiting to happen. Restructured UpdatedCallback implementation. 

**Next Day's Goal(s)** Create cards and implement a RecyclerView in a staggered layout. Overall revamping of UI. Look into JobScheduler to replace TimerTask. 

**Link to work:** [Switched to a Handler](https://github.com/jgarcia162/Updated/commit/e5eca6b1c821e4e6564c1eaf8a808058e93f7745)<br>[Restructured Callback](https://github.com/jgarcia162/Updated/commit/30d552814447d9125e961bbfb9e26c3630917172)

### Day 4: February 2, 2017

**Today's Goal:**  Create cards and implement a RecyclerView in a staggered layout. Overall revamping of UI. Look into JobScheduler to replace TimerTask. 

**Today's Progress:** Implemented CardViews, StaggeredGridLayoutManager for RecyclerView. Found a way to grab favicon from webpage and use as display image. Webview in CardView proved to not be aesthetically pleasing. Learned about GridItemDecorations, a way to customize the way items are laid out in the RecyclerView by adding edge shadows and spacing between items. Found a bug where my MainActivity was being recreated upon clicking a notification. Fixed this by adding `launchMode:singleInstance` to the activity in the manifest. Not sure if this is the best approach but it works! 

**Next Day's Goal(s)** Improve UI and work on Page Details Fragment, maybe implement JobScheduler

**Link to work:** [Updated UI with Cardviews in a StaggeredGridLayout](https://github.com/jgarcia162/Updated/commit/cf9eaa49f3290c73f1bba0bbd77b91857363d70f)<br>[Fixed multiple activity bug](https://github.com/jgarcia162/Updated/commit/679c0a55d4b1bfdfd756818f3c0d6c18aed0031f)

### Day 5: February 5, 2017

**Today's Goal:**  Improve UI and work on Page Details Fragment, maybe implement JobScheduler

**Today's Progress:** Didn't touch UI. Spent a lot of time trying to implement OkHttp3 but decided to stick with AsyncTask. Started work on DetailsFragment. May need to consider some restructuring for smooth navigation between MainActivity, DetailsFragment, and UserSettings.

**Next Day's Goal(s)** Continue work on DetailsFragment and consider navigation flow.

**Link to work:** [Began Implementing DetailsFragment](https://github.com/jgarcia162/Updated/commit/c00b67c7067fe5b3efff0966dde093bd337d2664)

### Day 6: February 6, 2017

**Today's Goal:**  Continue work on DetailsFragment and consider navigation flow

**Today's Progress:** Added a second activity to load PageDetailsFragment. Notification string displaying multiple page titles(bug). Began working on SharedPreferences persistence.

**Next Day's Goal(s)** Fix notification bug and implement settings fragment and SharedPreferences for persistence.

**Link to work:** [Implemented DetailsFragment](https://github.com/jgarcia162/Updated/commit/ddeb15fba69b3749b471bc514e4a6aee56d564ac)

### Day 7: February 9, 2017

**Today's Goal:**  Fix notification bug and implement settings fragment and SharedPreferences for persistence.

**Today's Progress:** Notification bug resolved. Implemented SharedPreferences persistence for default notes, update frequency, and favicon. Created a constants class to hold default values. 

**Next Day's Goal(s)** Create layout for PreferencesFragment and implement menu buttons for preference navigation. Add default photo for null favicons. Add toggle button to PreferencesFragment, make URL editable in PageDetailsFragment.

**Link to work:** [Added PreferencesFragment and some data persistence through SharedPreferences](https://github.com/jgarcia162/Updated/commit/beb47554ee88c90084e3a08ab0f438ccaf1ab3ad)
