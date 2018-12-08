### Day 24: December 7, 2018
**Today's Goal:** Add clear all filters button for ChipsDialogFragment. 

**Today's Progress:** added clear button for filter chips

**Links to work:** 
* [WIP adding clear button](https://github.com/jgarcia162/Bookworm/commit/a4bf03544edb4a1ae93e892e84a23b47c7042c97)

**Next Day's Goal(s):** Finish clear button

### Day 23: December 4, 2018
**Today's Goal:** Load persisted filters from preferences and display when ChipsDialogFragment is inflated. 

**Today's Progress:** Selected filter chips are saved to SharedPreferences via a SharedPreferencesHelper. When the ChipsDialogFragment is shown, previously selected filters are loaded. Changed ChipGroup.addChips extension function to accept a List of Chips as parameter. 

**Links to work:** 
* [Persisting selected filters](https://github.com/jgarcia162/Bookworm/commit/4fcdbae8e0a4118bf02b074bb3aacf96a71298c5)

**Next Day's Goal(s):** Add clear all filters button for ChipsDialogFragment. 

### Day 22: December 3, 2018
**Today's Goal:** Persist filtered chips. 

**Today's Progress:** Created a PreferencesHelper to persist Filter lists. 

**Links to work:** 
* [Created prefs helper](https://github.com/jgarcia162/Bookworm/commit/3b272bc82f15c99b401e46f892d3b016287d8b0c)

**Next Day's Goal(s):** Load persisted filters from preferences and display when ChipsDialogFragment is inflated. 

### Day 21: December 2, 2018
**Today's Goal:** Finish multiple list Rx stream"

**Today's Progress:** User can now filter best-sellers by selecting chips. Working on persisting the selected chips. 

**Links to work:** 
* [List filter working](https://github.com/jgarcia162/Bookworm/commit/3f5128c479b743e84cb73aa92caa2d5f6f223dac)

**Next Day's Goal(s):** Persist filtered chips. 

### Day 20: December 1, 2018
**Today's Goal:** Work on "Current reading RV"

**Today's Progress:** Added "Done" and "Cancel" buttons to ChipsDialogFragment. Created function to load multiple lists based on Chips selected in the dialog fragment. Using RxJava to load each list then combine results(WIP). 

**Links to work:** 
* [WIP multilist Rx stream](https://github.com/jgarcia162/Bookworm/commit/6196c713eeccb6dba77f25ad97e2d77085c85b7b)

**Next Day's Goal(s):** Finish multiple list Rx stream

### Day 19: November 30, 2018
**Today's Goal:** Fix Chips bug in FeedPresenter test.

**Today's Progress:** Chips dialog now shows and selected chip loads corresponding list then dismisses after loading.

**Thoughts:** When inflating the layout for a DialogFragment, if using ConstraintLayout, the constraints must be added to the ConstraintLayout itself. 

**Links to work:** 
* [ChipsDialogFragment loads selected list](https://github.com/jgarcia162/Bookworm/commit/a96839dd7bae188a47ef7c7b5062eb21be6338c8)

**Next Day's Goal(s):** Work on "Current reading RV"

### Day 18: November 28, 2018
**Today's Goal:** Fix Chips bug in FeedPresenter test.

**Today's Progress:** Created a custom DialogFragment to display all the best-sellers list names as Chips for filtering best-sellers. Added a clickable filter icon. The custom DialogFragment is receiving the data and adding Chips to the ChipGroup, confirmed this through log messages. However the fragment layout is not displayed. 

**Links to work:** 
* [WIP add ChipsDialogFragment](https://github.com/jgarcia162/Bookworm/commit/2851da39b8f7433bb208aebe7471853f80c69ef6)

**Next Day's Goal(s):** Fix ChipsDialogFragment bug.

### Day 17: November 27, 2018
**Today's Goal:** Fix Chips bug in FeedPresenter test.

**Today's Progress:** Best Sellers Chips are added to ChipGroup when FeedFragment is started. Clicking a Chip will load list data. 

**Links to work:** 
* [Best Seller Chips added to ChipGroup](https://github.com/jgarcia162/Bookworm/commit/1da9893dc6db24763598c5ab15fa73f4a1ed827b)
* [Fixed Tests](https://github.com/jgarcia162/Bookworm/commit/2348c977df7b24220abc4cc30d86f76e83618d9b)
* [Migrated to Androidx dependencies](https://github.com/jgarcia162/Bookworm/commit/006b639fc3eddb63c825852489b1be9c00f4191a)
* [Chip categories load on click](https://github.com/jgarcia162/Bookworm/commit/f5deec963ce1395dc3dee1d0f8baca160e62f626)

**Next Day's Goal(s):** Create fragment for chip categories

### Day 16: November 26, 2018
**Today's Goal:** Fix Chips bug in FeedPresenter test.

**Today's Progress:** BestSellers overview data loads on FeedFragment start. Edited TimesBook class to include abstract variables. This is the base class for all the book models in NY Times API. 

**Links to work:** 
* [Overview data loads onStart](https://github.com/jgarcia162/Bookworm/commit/443ded62e6a6bd0b25626e93d9cb519be075d8e7)

**Next Day's Goal(s):** Work on ChipsGroup scroll view. 

### Day 15: November 22, 2018
**Today's Goal:** Finish tests for FeedFragment, set up FeedFragment.

**Today's Progress:** Worked on more tests for FeedFragment. Wrote a function to add new chips dynamically. Ran into a bug related to this Chips function. 

**Links to work:** 
* [ChipGroup function, best sellers list function](https://github.com/jgarcia162/Bookworm/commit/eca1818975fe6eb4d8a8a44a7939806bcb26bdd1)
* [NYTimesBook class, edited tests, and feedfragment](https://github.com/jgarcia162/Bookworm/commit/0675ae41b0e4d3982249b7b83346ae428310dc80)
* [WIP Chips test](https://github.com/jgarcia162/Bookworm/commit/9150e2d9023b00a75e425ee7b0f2ec5f941842ea)

**Next Day's Goal(s):** Fix Chips bug in FeedPresenter test.

### Day 14: November 21, 2018
**Today's Goal:** Finish test for FeedFragment

**Today's Progress:** Wrote tests for FeedFragment. Made edits to FeedFragment functions. Added ChipGroup to FeedFragment.  

**Links to work:** 
* [Tests, ChipGroup, Functions](https://github.com/jgarcia162/Bookworm/commit/8806febeffd344830d4433ab10a567dfd41becf0)

**Next Day's Goal(s):** Finish tests for FeedFragment, set up FeedFragment.

### Day 13: November 20, 2018
**Today's Goal:** Complete GenericAdapter and test

**Today's Progress:** Completed GenericAdapter, worked on FeedFragment, wrote new dagger provides methods for Presenters, wrote test for FeedFragment but am running into an error.

**Links to work:** 
* [Working on tests, and other edits](https://github.com/jgarcia162/Bookworm/commit/81b451655498b83433c65c22a3d366d4fda540ee)

**Next Day's Goal(s):** Finish test for FeedFragment.

### Day 12: November 17, 2018
**Today's Goal:** Implement logic for FeedFragment

**Today's Progress:** Added a README 

**Links to work:** 
* [Added README](https://github.com/jgarcia162/Bookworm/commit/99d9c8935764f6c2c1490d96f8babc6c86717b61)
* [Set up Dagger 2 architecture](https://github.com/jgarcia162/Bookworm/commit/aa5e3b24e5509437087ee99088882a7400a72357)
* [Creating generic adapter](https://github.com/jgarcia162/Bookworm/commit/5152ea54b442889140e2e95c1ac5672fdb015e9f)

**Next Day's Goal(s):** Complete GenericAdapter and test

### Day 11: November 16, 2018
**Today's Goal:** Write test for NY Times API, implement logic for FeedFragment

**Today's Progress:** Edited NY Times API models, API tests, removed gradle.properties from tests branch

**Links to work:** 
* [Edited API tests and NY Times API models](https://github.com/jgarcia162/Bookworm/commit/99d9c8935764f6c2c1490d96f8babc6c86717b61)
* [Added gradle.properties to gitignore](https://github.com/jgarcia162/Bookworm/commit/86fa7da4032b0b9315d4e06748310e005c287c86)

**Next Day's Goal(s):** Implement logic for FeedFragment

### Day 10: November 15, 2018
**Today's Goal:** Continue Google Books Api setup

**Today's Progress:** Added NY Times Books API to get best sellers list

**Links to work:** 
* [Added NY Times Books API](https://github.com/jgarcia162/Bookworm/commit/48a77a3ffe01de0bde961f888a2fd70665d142e5)

**Next Day's Goal(s):** Write test for NY Times API, implement logic for FeedFragment

### Day 9: November 13, 2018
**Today's Goal:** Create API client wrapper class and Retrofit API services

**Today's Progress:** Wrote a test for Google Books API. 

**Links to work:** 
* [Added BooksApi test](https://github.com/jgarcia162/Bookworm/commit/b681194715441989a3e78ae8bbe8892002084de3)

**Next Day's Goal(s):** Continue Google Books Api setup

### Day 8: November 12, 2018
**Today's Goal:** Create API client wrapper class and Retrofit API services

**Today's Progress:** Created ApiClient wrapper class, BooksApi service interface, models for Google Books API responses. Added API key as BuildConfig gradle property.

**Links to work:** 
* [ApiClient wrapper class and Books API models](https://github.com/jgarcia162/Bookworm/commit/418e828309b9d29fc4946760ef16534f246f243b)

**Next Day's Goal(s):** Write tests for BooksApi 

### Day 7: November 9, 2018
**Today's Goal:** Create BookDetails layout

**Today's Progress:** Created layout for Book Details

**Links to work:** 
* [Book Details layout](https://github.com/jgarcia162/Bookworm/commit/35c0b1a4e992be8a33ba2a1ddb1bbba5c7686e6c)

**Next Day's Goal(s):** Create API client wrapper class and Retrofit API services

### Day 6: November 7, 2018
**Today's Goal:** Finish new UI elements for added features and continue MVP set-up.

**Today's Progress:** Made more UI changes, added a progress bar to book list item layout. Added colors

**Links to work:** 
* [Some UI changes](https://github.com/jgarcia162/Bookworm/commit/37d336646f9a2f91d0e631061620e38356757408)

**Resources Used:** 
* [UI Inspiration](http://collectui.com/designs)

**Next Day's Goal(s):** Create BookDetails layout

### Day 5: November 6, 2018
**Today's Goal:** Finish new UI elements for added features and continue MVP set-up.

**Today's Progress:** Made more UI changes, added a progress bar to book list item layout. Added colors

**Links to work:** 
* [Some UI changes](https://github.com/jgarcia162/Bookworm/commit/c8d79c76df573767df670629ca1e1fdfba2a8d0c)

**Resources Used:** 
* [Material Design Chips Guideline](https://material.io/design/components/chips.html)

**Next Day's Goal(s):** Continue UI edits.

### Day 4: November 5, 2018
**Today's Goal:** Finish MVP set-up and add new UI elements for added features.

**Today's Progress:** Made some changes to UI, added layout for FeedFragment and SearchFragment. Added BottomNavigationView for LibraryFragment. 

**Links to work:** 
* [Added bottom navigation](https://github.com/jgarcia162/Bookworm/commit/8aeb04fb01e4a86b343ddbad03d422c6604f56c9)
* [Added new layouts](https://github.com/jgarcia162/Bookworm/commit/d1b7eced37c034a4e9ccfcd84f54a91665637d9d)

**Next Day's Goal(s):** Finish new UI elements for added features and continue MVP set-up.

### Day 3: November 4, 2018
**Today's Goal:** Implement MVP design pattern

**Today's Progress:** Set up the skeleton for MVP design pattern. Thought of new functionalities to track progress and sort books. 

**Links to work:** 
* [Added BookDetails components](https://github.com/jgarcia162/Bookworm/commit/56a7e7aefdd5ec7c8a8452180cc0e46c7dbd457b)
* [Added Library components](https://github.com/jgarcia162/Bookworm/commit/ce287f37c9ad35451caeacb4e6384a0d47ba09dd)
* [Added Feed components](https://github.com/jgarcia162/Bookworm/commit/c013b6afd758f7f0522f680a1d7fa80f78199246)

**Thoughts:** It's important to flesh out the features I want to implement before starting to structure the app. While I'm figuring out the architecture I'm thinking of new ideas and this affects the way I approach the architecture. I learned to establish a list of the most fundamental features before building the skeleton. 

**Next Day's Goal(s):** Finish MVP set-up and add new UI elements for added features.

### Day 2: November 3, 2018
**Today's Goal:** Update UI layouts

**Today's Progress:** Added menu options and edited UI layouts. These layouts will be polished later. 

**Links to work:** 
* [Edited RV Card Layout](https://github.com/jgarcia162/Bookworm/commit/e2f1632d276c00c11c32d9af0fa6fcd62901f6d6)
* [Added menu options](https://github.com/jgarcia162/Bookworm/commit/0b8afe9e49dd0d065f83b78581412cf73f7f9e1f)

**Next Day's Goal(s):** Implement MVP design pattern

### Day 1: November 2, 2018
**Today's Goal:** Implement Room database

**Today's Progress:** Implemented Room database and necessary TypeConverters. TypeConverters allow us to save complex data types such as Lists or custom data classes in our Room database 

**Resources Used:** 
* [TypeConverter Guide](https://medium.com/@toddcookevt/android-room-storing-lists-of-objects-766cca57e3f9)
* [Room Documentation](https://developer.android.com/training/data-storage/room/)

**Links to work:** 
* [Room database and TypeConverters](https://github.com/jgarcia162/Bookworm/commit/495ec6ff93c3ca03cf57ffe8604ef644dd93abd7)

**Next Day's Goal(s):** Update UI layouts

### Day 0: November 1, 2018
**Today's Goal:** Restructure Bookworm app to include Android Jetpack Application Components. Start with implementing ViewModel for Book data class

**Today's Progress:** Implemented ViewModel for Book data class. Extracted all dependencies to [`dependencies.gradle`](https://github.com/jgarcia162/Bookworm/blob/master/gradle/dependencies.gradle)

**Resources Used:** 
* [ViewModel Overview](https://developer.android.com/topic/libraries/architecture/viewmodel)
* [Guide to app architecture](https://developer.android.com/jetpack/docs/guide)

**Links to work:** 
* [Created dependencies.gradle](https://github.com/jgarcia162/Bookworm/commit/fd4654e819716ea1bcd7511034a0a9e7754c23af)
* [Implemented BookViewModel](https://github.com/jgarcia162/Bookworm/commit/aaf5993bd0c54a2598c50d5d79d6f34892294e16)

**Next Day's Goal(s):** Implement Room database
