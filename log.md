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

### Day 8: February 16, 2017

**Today's Goal:**  Create layout for PreferencesFragment and implement menu buttons for preference navigation. Add default photo for null favicons. Add toggle button to PreferencesFragment, make URL editable in PageDetailsFragment.

**Today's Progress:** Created menu buttons, added default photo for empty favicons. I used a base activity to be able to inclue options menu in every activity without rewriting options menu logic. Using a second activity to house all the menu screens to avoid restructuring main activity as a fragment. 

**Today's Insight:** Proper planning and structuring beforehand proves to be extremely important. Started my app with one activity then ran into issues that could have been avoided if initial activity was a fragment instead. 

**Next Day's Goal(s)** Fix BaseActivity recreating bug. Add layout for SettingsFragment, and ContactFragment, begin implementing of SQL database.

**Link to work:** [Implemented Menu Options, BaseActivity, and Default Icons](https://github.com/jgarcia162/Updated/commit/28fbd56e7da2c9860d6997b0f14342e3426b1146)

### Day 9: February 18, 2017

**Today's Goal:**  Fix BaseActivity recreating bug. Add layout for SettingsFragment, and ContactFragment, begin implementing of SQL database.

**Today's Progress:** Got rid of BaseActivity, fixed recreation bug. Working on layouts. 
**Update:** Was supposed to work on layout rest of the day but got hung up on more unforeseen bugs (like this never happens). Added a verification for valid URLs, ran into favicon bug that duplicates favicon despite page url, did not get to layouts as intended.

**Next Day's Goal(s)** Fix favicon bug, work on layouts, begin SQL database

**Link to work:** [Fixed Activity onCreate bug](https://github.com/jgarcia162/Updated/commit/d1497e55a325503c0df834d5e9deca49e38ce1dd) <br>
[Added URL verification](https://github.com/jgarcia162/Updated/commit/0b23034c24fe4e1bbfeaa4ae6c4de1c4df95334d)

### Day 10: February 20, 2017

**Today's Goal:**  Fix favicon bug, work on layouts, begin SQL database

**Today's Progress:** Favicon bug gone, edited settings layout and page details layouts, changed default logo, begun implementing delete button. Implemented a CustomTabIntent for in-app browsing

**Next Day's Goal(s)** Begin SQL database, finish delete button implementation, finish settings layout

**Link to work:** [Favicon bug gone, new logo, customtabintent, edited page details](https://github.com/jgarcia162/Updated/commit/bb2d13fefb9eefdac05be1c5023fd5467869dd2a)

### Day 11: February 22, 2017

**Today's Goal:**  Begin SQL database, finish delete button implementation, finish settings layout

**Today's Progress:** Almost done with setting layout. Still need to implement delete function and db. Found that nasty favicon bug again. 

**Next Day's Goal(s)** Finish Setting layout, implement long-click for deleting a page.

**Link to work:** [Edited SettingsFragment layout](https://github.com/jgarcia162/Updated/commit/b7eedc2427f8b8f8fb5edee8a9bfd982bad1cecc)

### Day 12: February 24, 2017

**Today's Goal:**  Finish Setting layout, implement long-click for deleting a page.

**Today's Progress:** Redesigned setting page layout. Added social media and email buttons. Completed SettingsFragment, all settings now saved to SharedPreferences. Implementing delete page button. RecyclerView now has custom slide in from bottom animation.

**Next Day's Goal(s)** Implement delete page button. Add email intent and begin working on social media integration.

**Link to work:** [SettingsFragment complete](https://github.com/jgarcia162/Updated/commit/2093566f585aa91b5f54d2b1e285c7541aecaddb)
