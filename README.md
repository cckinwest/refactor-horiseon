# About this challenge
This challenge is to refactor the code of the webpage of Horiseon company.

# Overview
The webpage can run without any problems. However, the structure of the code is too complicated and need restructuring.

# Details of the important changes
## HTML
### Problems
1. <div> tag is overused.
2. <ul> should not be used to organize <a> in the header because it makes the code more complicated. Even worse, the style of <li> needed to be dealt.
3.  Unique class is given for each component which makes reduce readibility and css unnessarily long. Classes should not be used in this way.
### Solutions
1. Semantic elements are used to replace most of the div, for example <header>, <nav>, <section>, <article>, and <footer>. They express the purpose of different components clearly and make it easier for the browser to understand the code.
2. <div> is used to organize <a> instead.
3. For reusable components with the same styling, classes are given. For example, the original classes "search-engine-optimization", "online-reputation-management", and "social-media-marketing" are now all under the same class "service-article"; the original classes are now used as id instead. Important unique component like company name is given the id "company-name" for easier refering.

## CSS
### Problems
1. Due to the restructuring in the header in html, the css is changed as well.
2. Some attributes are appeared repetitively. For example, the "color" appears many times, which is unnessary as most of the texts have the same color.
3. Repetitive styling made the css too long. It's not necessary for styling .search-engine-optimization, .online-reputation-management, and .social-media-marketing separatly as they share the same styling.
### Solutions
1. The original styling about <ul> and <li> are deleted. Selectors are also simplified and renamed more sensibility. For example, .header h1 is changed to "company-name", 
.header h1 .seo is changed to "company-name-middle".
2. Some attributes are reorganized more reasonably. For example, The "color" now only appears in the "body".
3. The styling of .search-engine-optimization, .online-reputation-management, and .social-media-marketing is now grouped together into "service-article". The css now becomes much simplier and easier to be managed. Similar changes have been made for the right column as well.

# Appearance of the refactored page after the changes
![appearance of the refactored Horiseon's webpage](./assets/images/webpage.png)

# URL of the refactored webpage
[Horiseon's webpage](https://cckinwest.github.io/refactor-horiseon/)