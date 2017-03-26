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

**Link to work:** [SettingsFragment layout complete](https://github.com/jgarcia162/Updated/commit/2093566f585aa91b5f54d2b1e285c7541aecaddb)

### Day 13: March 1, 2017 

**Today's Goal:**  Implement delete page button. Add email intent and begin working on social media integration.

**Today's Progress** Implemented Realm database with a RealmDatabaseHelper wrapper. Implemented delete button and reset defaults button with alert dialog.  

**Thoughts** This last session actually spread over a couple days. I didn't want to count this as a day until the work was completed. This was a big lesson in the importance of prioritizing and realized it is probably a good idea to build your database early on. After this implementation I noticed many issues which I had before could have been completely avoided had the db been built first. Realm was not difficult to learn and it certainly proved more flexible than a traditional SQL db. 

**Next Day's Goal(s)** Work on contacts section of Settings Fragment. Implement a long press to delete and "delete all" functionality

**Link to work:** [Realm database implemented](https://github.com/jgarcia162/Updated/commit/f417e4ee39ae4643a7c1c16f8f569b55109af713)

### Day 14: March 3, 2017 

**Today's Goal:**  Work on contacts section of Settings Fragment. Implement a long press to delete and "delete all" functionality

**Today's Progress** Did not get to contacts section. Begun implementation of a custom MultichoiceListener for RecyclerView. Functionality almost complete. Running into a defaultClickListener error where holder is not changing position. On click delivers the same position for every viewholder.  

**Next Day's Goal(s)** Finish implementing Multichoice functionality for deletion implementation. Fix on click bug.

**Link to work:** [Begun Multichoice Functionality](https://github.com/jgarcia162/Updated/commit/2a927f09e1e84eb7f29b19e1114abfdce7f445f9)<br>
[MultichoiceRecyclerView Library](https://github.com/dvdciri/MultiChoiceRecyclerView)

### Day 15: March 5, 2017 

**Today's Goal:**  Finish implementing Multichoice functionality for deletion implementation. Fix on click bug.

**Today's Progress** Decided to put off the Multichoice functionality for the next day, instead I implemented an alert dialog box that will show whenever the user has no network connection and tries to manually refresh. Original idea was to implement OkHttp and use a custom callback to handle the onFailure of a network request to show the dialog but this proved much too complicated without introducing potential memory leaks via static Context references.

**Next Day's Goal(s)** Implement Multichoice functionality

**Link to work:** [AlertDialog implemented](https://github.com/jgarcia162/Updated/commit/03f66b01adcf8b6363d16ad161c575b873cd5284)

### Day 16: March 7, 2017 

**Today's Goal:**  Implement Multichoice functionality

**Today's Progress** After fixing minor UI bugs I began to tackle this Multichoice functionality. Made some progress, now just need to implement buttons for multi-editing.

**Next Day's Goal(s)** Implement Multichoice functionality multiediting

**Link to work:** [Editing Multichoice Toolbar](https://github.com/jgarcia162/Updated/commit/1730b9a371c6dc431be0b14c4edee4c416adabb5)

### Day 17: March 9, 2017 

**Today's Goal:**  Implement Multichoice functionality multiediting

**Today's Progress** I just got my hands on a Raspberry Pi 2 and in the excitement I put off working on my app to get a RetroPie up and running because I miss my childhood video game binges. My first time working with hardware so the learning curve is there but online tutorials are very helpful. Still working on this but might not finish today. 

**Next Day's Goal(s)** Finish RetroPie build

**Resources:** [Tutorial](https://github.com/retropie/retropie-setup/wiki/First-Installation)

### Day 18: March 10, 2017 

**Today's Goal:**  Finish RetroPie build

**Today's Progress** Retropie build done. Installed Playstation, SNES, Dreamcast, GBA, and MAME emulators. Added animation to custom tab browser. Fixed SSL exception thrown by HTTP Connection by implementing default "http" scheme for URL inputs. I found the logic for update refreshing is not working as intended. 

**Next Day's Goal(s)** Fix logic for checking updates. Continue work on Multichoice toolbar.

**Resources:** [RetroPie Photo](https://pbs.twimg.com/media/C6iWrt9VoAAryNS.jpg)<br>
[Added animation to custom tab](https://github.com/jgarcia162/Updated/commit/900f2945029985afedb4ac97007a38ff3e5d432a)

### Day 19: March 11, 2017 

**Today's Goal:**  Fix logic for checking updates. Continue work on Multichoice toolbar

**Today's Progress** Got side-tracked and decided to figure out how a swipe left and right feature could be implemented on a CardView. Found a sample project online and scraped off the excess fat. Managed to create a simple implementation that, in theory, could be attached to any View object.

**Next Day's Goal(s)** Fix logic for checking updates. Continue work on Multichoice toolbar.

**Link** [My Implementation](https://github.com/jgarcia162/SwipePractice)<br>
**Resources** [Original Sample Project SwipeDeck2](https://github.com/aaronbond/SwipeDeck2)

### Day 20: March 14, 2017 

**Today's Goal:**  Fix logic for checking updates. Continue work on Multichoice toolbar

**Today's Progress** Fixed update checker logic. No more duplicate notifications. Removed IG contact button and started implementing Twitter integration using Twitter4J library. Running into a callback issue. 

**Next Day's Goal(s)** Finish Twitter integration

**Link** [Started Twitter integration](https://github.com/jgarcia162/Updated/commit/0853145bae2f2f24ab4343a1186412783649a6c1)<br>

**Resources** [Twitter4J Library](http://twitter4j.org/en/index.html)

### Day 0: March 21, 2017 

**Note:** Resetting to day 0 because I missed more than two days 

**Today's Goal:**  Finish Twitter DM integration

**Today's Progress** Twitter DM integrated. Users can send me a direct message on twitter as a form of contact. Intents for github and email also added.   

**Next Day's Goal(s)** Replace intents with in-app message sending via dialog box.

**Link** [Finished Twitter integration and contact intents](https://github.com/jgarcia162/Updated/commit/9682e9eae560c8cdc1e920a38f02580d53e76c8b)

### Day 1: March 23, 2017 

**Today's Goal:**  Replace intents with in-app message sending via dialog box.

**Today's Progress** I decided to ergo the dialog box message sending functionality. This, while a somewhat convenient feature, proves to be uncessesary. I began implementing a button layout to give users the choice of selecting all items in the list and deleting/untracking multiple items at once. Finished implementing the select all and deselect all buttons. Created a ButtonListener interface to allow communication between the adapter and main activity. 

**Next Day's Goal(s)** Implement delete and untrack buttons.

**Link** [Added button layout and implemented select/deselect](https://github.com/jgarcia162/Updated/commit/f9cdd624056d6b360ee924cf031e55d24fde3707)

### Day 2: March 25, 2017 

**Today's Goal:**  Implement delete and untrack buttons.

**Today's Progress** Delete and Untrack buttons complete. Decoupled UpdatedCallback from UpdatedBroadcastReceiver. Found one bug in multichoice feature. After adding a new page, long-click to select feature doesn't work, app must be restarted for feature to apply to newest items. 

**Next Day's Goal(s)** Fix multichoice bug. Begin redesign of UI. 

**Link** [Completed delete and untrack buttons, decoupled UpdatedCallback](https://github.com/jgarcia162/Updated/commit/ce836450ef6106e996bd3dbdb4750352768c9e4c)
