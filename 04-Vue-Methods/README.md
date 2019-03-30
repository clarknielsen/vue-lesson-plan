## Vue Methods

* In this app, users can click on the button to add fruits to the list. This is accomplished by adding an onclick listener to the button. However, this isn't really following Vue best practices, because we are 1) affecting the DOM directly instead of letting Vue do it and 2) running the risk of our logic and layout getting lost as the codebase grows.

* Let's rewrite this the "Vue way" by using a `v-on:click` directive and adding a method to our Vue instance. Again, reference the documentation for help: <https://vuejs.org/v2/guide/>

* **BONUS:** Disable the button after the first click so users can't keep adding the same fruits over and over. You may need to do a bit of Googling on this one.
