## Introduction to Vue.js

### Overview

Going into this lesson, students should already have a good understanding of HTML, Javascript, and jQuery. Prior knowledge of other JS frameworks isn't expected.

At the end of the lesson, students should be able to articulate why JS frameworks are useful and be able to set up a simple Vue.js example on their own.

- - -

### 1. Instructor Do: JS Frameworks (5 min)

* Ask students to recap the purpose of jQuery.

  * _It gives us an easier syntax to perform DOM manipulation._

* Explain that there are many tools out there that aim to serve a similar purpose: to make writing and maintaining Javascript code easier. That's when we get into what are called "Javascript frameworks."

### 2. Students Do: Research (10 min)

* Have students work in pairs to research/answer the following questions:

  1. What is a Javascript framework?

  2. Why would jQuery not be considered a framework?

  3. What are the most popular JS frameworks today?

  4. When should you (or should you not) use a JS framework?

### 3. Instructor Do: Recap Answers (5 min)

* Call on students to provide answers to the questions above. Feel free to add to their answers if they weren't complete enough.

  1. 

  2. 

  3. 

  4. 

### 4. Instructor Do: Introduce Vue (15 min)

* Navigate to <https://vuejs.org/> (and Slack it out at the same time). Explain that we'll be focusing on Vue.js in this class. That doesn't mean Vue.js is necessarily _the best_ JS framework. Emphasize that the best framework is the one that makes the most sense to you and your team or best fits your project. Vue.js just happens to have a lighter learning curve, and once you master one framework, it's relatively easy to pick up others.

* If you have any experience with React and/or Angular, you may want to briefly explain that other frameworks tend to require more setup to get started and are often paired with additional technologies you have to learn at the same time. Vue, on the other hand, is more straightforward.

* To demo that, navigate to the "Get Started" page at <https://vuejs.org/v2/guide/> and scroll down to the CDN link:

  ```html
  <!-- development version, includes helpful console warnings -->
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  ```

* Point out that, like jQuery, this is all we really need to get started, but because Vue is a _framework_ and not just a library, we get a lot more power out of the CDN.

* Either create a new file from scratch or use `02-Vue-Intro/basic.html` to demo copying the CDN into an HTML file. Highlight that, with Vue, we leave {{ placeholders }} in the HTML for data that Vue (Javascript) will fill in later:

  ```html
  <div id="app">
    {{ message }}
  </div>
  ```

* Then show how we build Vue instances in JS and attach them to the DOM, highlighting that Vue() is just a constructor that takes in an object:

  ```js
  var app = new Vue({
    el: "#app",
    data: {
      message: "Hello World"
    }
  });
  ```

* When the page loads, the message "Hello World" will appear in the div. Add 1-2 more placeholders and data properties to drive home this point.

### 5. Everyone Do: Pulse Check (5 min)

* Ask the class, "How could we have accomplished the same thing with regular Javascript or jQuery?" Give students time to come up with a logical answer, something like: `$("#app").html("Hello World")`.

* Point out that doing things the "Vue way" probably feels like more work so far. When dealing with JS frameworks, the benefits aren't apparent when doing small examples, but as your app grows in size and complexity, you'll come to appreciate what frameworks do for you.

### 6. Instructor Do: Vue Directives (10 min)

* Now open `01-Vue-Intro/directives.html` and highlight the directive on line 11:

  ```html
  <div id="app" v-if="show">
  ```

* Explain that directives are special HTML attributes that Vue understands and will do something special with. In this case, "v-if" controls the visibility of this div based on the true/false value of "show." In the Vue instance below, change show to be false and reload the page to show that the div is now gone.

* Uncomment the setInterval to show how we can not only change the value of show programmatically but that doing so also changes the visibility of the div:

  ```js
  setInterval(function() {
    app.show = !app.show;
  }, 1000);
  ```

* Explain that directives are how we can make "dynamic templates." We no longer have to "target and update" like we did with jQuery. With Vue, changing the data will automatically change the DOM.

### 7. Students Do: Vue Lists (15 min)

* Direct students to activity `03-Vue-Lists`. This is a chance for them to practice using other Vue directives. They'll need to reference the official documentation for help. Also make sure they attempt the bonus (using a v-if inside of a v-for).

### 8. Instructor Do: Review Solution (5 min)

### 9. Students Do: Vue Methods (15 min)

* Open `04-Vue-Methods/Unsolved/methods.html` and demo that we're now adding the fruits via a button click instead of a timeout. However, we've gone against Vue best practices to do this. We should really be using Vue methods and directives instead.

* Let students know that this next activity is to rewrite/refactor this small example.

### 10. Instructor Do: Review Solution (5 min)
