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
