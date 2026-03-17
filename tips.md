# Taylor Tips

More to come :)

1. Make sure you enable `Full accessibility tree view in Elements panel` in Chrome's DevTools Settings (under `Experiments`).
    - This will provide you with a small button with a person icon in your Elements panel that shows the page as an accessibility tree.

2. If you are using a Mac, always show your scrollbars so you don't miss a user experience specific to non-Mac devices. To do this, go to System Settings, then Appearance, and select "Always" under "Show scroll bars".

3. Chrome's DevTools has a global search function hidden in the bottom pane where the Console usually shows. To make the pane visible, focus on the Chrome DevTools and hit the `Esc` key. Once you see the Console pane, click on the three dots settings indicator on the top left. Select the "Search" list item from the dropdown list.

4. The React DevTools have multiple great helpers for understanding your components:
    -  Check the `Highlight updates when components render.` checkbox to see a flash each time a component renders. This can be a great way to detect hidden re-render conditions and know if your data architecture is causing unnecessary full page re-renders on change.
    -  Check the `Always parse hook names from source` checkbox to have better descriptions of your custom hooks in the DevTools UI. *Note that this doesn't work with Next.js because of the way that webpack is creating sourcemaps.*
    -  Check the `Record why each component rendered while profiling.` checkbox to enrich your React profiler data with details on why the component rendered.

5. Network Panel
    -  I generally recommend having `Disable cache` checked for dev purposes. This will get you closest to experiencing what a fresh user would see hitting your site when you have the Chrome DevTools open.
    -  In the `More Filters` dropdown, you can check `Hide data URLs` and `Hide extension URLs` to reduce the amount of junk you have to sift through in the Network panel.
    -  Click on the top right cog in the Network Panel. Ensure that `Overview` and `Screenshots` are checked. These will give you clear insights into the user's experience at each step of the request waterfall.
    -  Checking `Preserve log` can help when testing redirects, since page loads usually clear the Network panel.
    -  Any Network Request can be blocked by right clicking on the request and selecting `Block request URL` or `Block request domain`. This is a great way to test error handlers or diagnose slowness.
    -  Network Overrides can be set up via right clicking the request as well, which enables you to override request headers and content.
        -  Headers can also be edited in the "Headers" panel that opens when clicking on a request.
    -  Wondering what component triggered a request? Click on the request, change to the `Initiator` tab, and you will see the JS trace of the request initiator.

6. Snippets
    -  Hold `CMD + SHIFT + P` to open the Command panel in Chrome DevTools
    -  Type `Show Snippets`
    -  Add any commonly used DevTools Console snippets you use
    -  Hold `CMD + SHIFT + P` again to open the Command panel in Chrome DevTools
    -  Delete the right arrow `>` and replace with an exclamation point `!`
    -  Search for the snippet you want to run and run it from any pane in your Chrome DevTools!

7. Coding Tips
    -  When you need to log a value, writing it as an object will automatically add a label to your message: `console.log({ yourVariableName })`
