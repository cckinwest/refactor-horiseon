# About this challenge
This challenge is to refactor the code of the webpage of Horiseon company.

# Overview
The webpage can run without any problems. However, the structure of the code is too complicated and need restructuring.

# Details of the important changes
## HTML
### Problems
1. div tag is overused.
2. Unique class is given for each component which makes reduce readibility and css unnessarily long. Classes should not be used in this way.
3. The webpage is not responsive.
### Solutions
1. Semantic elements are used to replace most of the div, for example header, nav, section, article, and footer. They express the purpose of different components clearly and make it easier for the browser to understand the code.
2. For reusable components with the same styling, classes are given. For example, the original classes "search-engine-optimization", "online-reputation-management", and "social-media-marketing" are now all under the same class "service-article"; the original classes are now used as id instead. Important unique component like company name is given the id "company-name" for easier refering.
3. A menu button is created and a menu-content is created to organized the links.

## CSS
### Problems
1. Due to the restructuring in the header in html, the css is changed as well.
2. Some attributes are appeared repetitively. For example, the "color" appears many times, which is unnessary as most of the texts have the same color.
3. Repetitive styling made the css too long. It's not necessary for styling "search-engine-optimization", "online-reputation-management", and "social-media-marketing" separatly as they share the same styling.
4. Css should be fixed for responsive design.
### Solutions
1. The original styling about ul and li are deleted. Selectors are also simplified and renamed more sensibility. For example, .header h1 is changed to "company-name", 
.header h1 .seo is changed to "company-name-middle".
2. Some attributes are reorganized more reasonably. For example, The "color" now only appears in the "body".
3. The styling of "search-engine-optimization", "online-reputation-management", and "social-media-marketing" is now grouped together into "service-article". The css now becomes much simplier and easier to be managed. Similar changes have been made for the right column as well.
4. Media queries are made to change the style of menu, the left and right columns.

# Appearance of the refactored page after the changes
![appearance of the refactored Horiseon's webpage](./assets/images/webpage.png)

# Apperance of the refactored page after adding responsive design
![appearance of the refactored Horiseon's webpage when the width of the page is 1024px](./assets/images/webpage-1024.png)
![appearance of the refactored Horiseon's webpage when the width of the page is 768px](./assets/images/webpage-768.png)

# URL of the refactored webpage
[Horiseon's webpage](https://cckinwest.github.io/refactor-horiseon/)