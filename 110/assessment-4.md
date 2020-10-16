In learning all of the non-standard aspects of web development that we have to look out for, despite web development being a standard way to create user interfaces across platforms, I have come to understand that building other platform specific user interfaces will be even more challening and irregular. There will likely be even more non-standard aspects across platforms that could lead to many more headaches and roadblocks that require serious thinking to work around. 


```
@media only screen and (min-width: 401px) and (max-width: 960px) {
   .sign-up{
       width: 50%;
   }
}
```
```
@media only screen and (min-width: 961px) {
    .sign-up {
        height: 200px;
        order: 1;
    }
}
```
The user agent will decide whether to use the rulesets or not based on the the rules defined by the media features (`(max-width:960px)`). If the conditions stated by the media features are true, then the user agent will use those rulesets. For example, the user agent will only use the rules of the first media querie for a screen and only if the screen width is between 401 pixels and 960 pixels. If any of those conditons are not met, the ruleset will not be used.


I think that it is better to define breakpoints using the specific content on a site because there really is no standard to use when it comes to devices. Take phones for example. While only a few years ago, most phone screens were relatively similar, now phone screens come in all sorts of shapes and sizes, making using a standard device size extremely difficult. 