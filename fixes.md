1. Removed 'true' condition so that this only triggers when window.Promise is 'false' previsouly it wil be all ways true and will load the polyfill bundle in every browser 

2. Removed duplicate jquery declaration and file from the repository

3. Removed heavy libraries moment.js and lodash.js because it is not used anywhere in the website

4. Removed font preload because it is not used anywhere

5. Removed unwanted fonts and its files and kept the only required font files which are used in the website

6. Added lazy loading to images

7. Compressed images to webp

8. Removed duplicate file (texture-copy.webp)

9. Removed @import url('vendor-framework.css');

10. Removed duplicate jquery file and its declaration from app.js

11. Fixed innerHTML += in a loop which fixied the infinite loading problem

12. Fixed unbounded array which fixied the memory leak problem

13. Removed resize event listener because it is not used anywhere

14. Removed Duplicated init call because it is not reqired

15. I don't understand the use case of this element , increasing the height of iv while seemsn not appropriate and unwnated
     Removed the scroll event listener because it is not reqired , since equalizeCardHeights is called only on the event listner he function is also removed

16. Used asynchrounous fetch to load reviews (also updated the function name as well)
    Updated functions that are using loadReviewsASync to asynchrounous 

17. Changed the condition to `now - last >= wait`

18. Increased throttle time to 5 secongs , now the data will be pushed to local storage in every 5 seconds

19. Created a new IntersectionObserver instance only once when page loaded.Since observer is initlized once we have the ability to track the element in an efficeint way. Also remove the throttle because it will not create a massive load at the page load .

20. Added analyticsBuffer clear function to clear the buffer after sync.

21. Reordered code , now when the modal is closed it first pushed and then it is removed from the DOM and the reference is also set to null

22. Used a new function to get the current screen refresh rate