# Startup

Elevator Pitch:
"Introducing AmniLive, the ultimate streaming platform for esports enthusiasts. With our state-of-the-art multi-stream feature, you can now follow all the action in your favorite esports games at the same time. Never miss a moment of the excitement as you can watch multiple players at a time, switching instantaneously between their viewpoints. Our platform offers a seamless viewing experience with high-quality streams and live stats. Plus, with a vast selection of esports titles, you'll have everything you need to stay on top of the competitive gaming scene. Join the future of esports streaming with AmniLive, sign up now!"

Key Features:

- Live Chat
- Multiple streaming perspectives/players/etc.
- User accounts with followed teams/players


Midterm Review Subjects:
- Bash
  - chmod
  - ls
  - sudo
  - ssh
  - Probably other very basic linux cmdline stuff
- HTML
  - Know what all the html elements stand for (div, a, b, etc.)
    - a: anchor
    - b: bold (bring attention)
    - div: division
    - p: paragraph
    - ol: ordered list
    - ul: unordered list
  - textContent is the text inside an element
  - ```<!-- an html comment -->```
- DNS
  - Record Type: CNAME or A
  - CNAME: Alias for another record
  - A: Points to an IP address
  - cs.byu.edu:
    - cs: subdomain
    - byu: domain name
    - edu: Top-Level domain
    - byu.edu: root domain
- CSS
  - Load fonts from Google (@import...)
  - Padding puts space around content of element
  - Margin puts space around the element itself
  - Order of Box Model: Margin - Border - Padding - Content
- Javascript
  - Formats for functions:
    - ```function f(x) {...}```
    - ```const f = function(x) {...}```
    - ```const f = (x) => {...}```
      - ```
        const f = y => ++y; // () and {} not necessary for simple functions
        console.log(f(3)); // Outputs 4
        ```
  - Understand async calls
    - .then((result) => {...}) Standard result
    - .catch((e) => {...}) error catch
    - .finally(() => {...}) will always get called
  - If there is no await then async will get "skipped"
    - ```
      const p = new Promis((resolve, reject) => {
        setTimeout(() {
          console.log( 'taco' ) ; // Third
          resolve(true);
        } , 10000);
      console. log( ' burger' ) ; // Will output first
      
      p
      .then((result) => console.log( 'shake' )) // Fourth
      .catch((e) => console.log( 'salad' )) // Fourth if error occurs in p
      .finally(() => console.log( 'noodles' )) // Outputs Fifth
      
      console.log( 'fries' ); // will output second
      ```
      
    - ```
      const p = new Promis((resolve, reject) => {
        setTimeout(() {
          console.log( 'taco' ) ; // Second
          resolve(true);
        } , 10000);
      
      try {
        console. log( ' burger' ) ; // Will output first
        await p();
        console.log( 'shake' ) // Third
      }
      catch {
        console.log( 'salad' )) // Third if error occurs in p
      }      
      
      console.log( 'fries' ); // will output Fourth
      ```
      
  - Know some RegEx for Filtering
  - Reduce: Takes array and reduces it down to one value
  - Map: Maps array to one of equal size with modified value for each cell (like adding 2 to every cell)
  - Filter: Takes array and outputs elements that match criteria (like regex)
  - Know document.AddEventListener
  
- JSON
  - Always double quotes around strings and keys: {"x":3}
