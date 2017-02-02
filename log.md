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

**Link to work:** [Switched to a Handler](https://github.com/jgarcia162/Updated/commit/e5eca6b1c821e4e6564c1eaf8a808058e93f7745)
                  [Restructured Callback](https://github.com/jgarcia162/Updated/commit/30d552814447d9125e961bbfb9e26c3630917172)

### Day 4: February 2, 2017

**Today's Goal:**  Create cards and implement a RecyclerView in a staggered layout. Overall revamping of UI. Look into JobScheduler to replace TimerTask. 

**Today's Progress:** Implemented CardViews, StaggeredGridLayoutManager for RecyclerView. Found a way to grab favicon from webpage and use as display image. Webview in CardView proved to not be aesthetically pleasing. Learned about GridItemDecorations, a way to customize the way items are laid out in the RecyclerView by adding edge shadows and spacing between items.  

**Next Day's Goal(s)** Improve UI and work on Page Details Fragment, maybe implement JobScheduler

**Link to work:** [Updated UI with Cardviews in a StaggeredGridLayout](https://github.com/jgarcia162/Updated/commit/cf9eaa49f3290c73f1bba0bbd77b91857363d70f)
