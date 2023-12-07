# Accessibility :: TabList Basics - Screen Readability

### requirements: 
> Please note that javascript is required to actually make the tab function as a tab BUT the exercise is really just for SR to read out that 1) which tab you are on 2) which tab content you are reading. For that you have no need of javascript.

### files:
- [tablist_final_code.html](tablist_final_code.html )
- [tablist_starting_code.html](tablist_starting_code.html )

### authoratative reference:
- [Mozilla - ARIA: tab role #example](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/tab_role#example)
- [w3.org - ARIA: Example of Tabs with Automatic Activation](https://www.w3.org/WAI/ARIA/apg/patterns/tabs/examples/tabs-automatic/)

### notes:
I believe the changes provided in [tablist_final_code.html](tablist_final_code.html ) are what is likely wanted.
As I was putting this together I remembered a discussion around the value of using ```aria-controls``` attribute on the elements given ```role="tab"``` ... where tab navigation was done in a manner where that ```aria-controls``` attribute is never truly leveraged.   In those cases it appeared that ```aria-labelledby``` attribute on the ```role="tabpanel"``` attributed element was enough to get screen readers to consistenly derive and declare the label/text provided on the tab item who's id(s) are passed in as the argument value.  I have found an old comment in notes that stated "We have reason to believe there might be benefit in leaving this attribute absent from the relevent code with this approach."

I believe this observation had some sort of merit, but I did not find any reference captured that pointed to why this was explored or arrived at, and I honestly don't remember.  I may extend this example to demonstrate a version with the ```aria-controls``` attribute removed.  If I do this, these should be considered experiments, as it looks like current examples at the sites I consider authoratative source still keep it in place...so I will assume that is the correct and desired pattern for this exercise.
