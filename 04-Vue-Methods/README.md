## Vue Methods

* In this app, users can click on the button to add extra fruits to the list. This is accomplished by adding an onclick listener to the button using vanilla JS. However, this isn't really following Vue best practices.

* Let's rewrite this the "Vue way" by using a `v-on:click` directive instead and adding a method to our Vue instance. Again, reference the documentation for help: <https://vuejs.org/v2/guide/>

* **BONUS:** Disable the button after the first click so users can't keep adding the same fruits over and over. You may need to do a bit of Googling for this one.

* **NOTE:** If done correctly, you should _not_ be using any `document.gets` or jQuery selectors.
