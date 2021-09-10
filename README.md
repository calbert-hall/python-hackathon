# Eyes Python Selenium Ultrafastgrid Tutorial
### Pre-requisites:

1. Python 3 is installed on your machine.  [Install Python 3.](https://realpython.com/installing-python/) 
2. Package manager pip is installed on your machine.  [Install pip](https://pip.pypa.io/en/stable/installing/)
3. Chrome browser is installed on your machine. [Install Chrome browser](https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&hl=en&oco=0)  
4. Chrome Webdriver is on your machine and is in the environment variable PATH. Here are some resources from the internet that'll help you.
   * [Download Chrome Webdriver](https://chromedriver.chromium.org/downloads), [Read the docs](https://splinter.readthedocs.io/en/0.1/setup-chrome.html), [Stackoverflow](https://stackoverflow.com/questions/38081021/using-selenium-on-mac-chrome), [Youtube](https://www.youtube.com/watch?time_continue=182&v=dz59GsdvUF8)
5. Git is installed on your machine. [Install git](https://www.atlassian.com/git/tutorials/install-git)
6. If you want to run example from IDE, install any IDE for Python (e.g. [PyCharm](https://www.jetbrains.com/pycharm/download/) )

### Run the example


# Hackathon Exercise!

* In this exercise, you'll be a Test Engineer looking to run tests on an e-commerce site, "Applifashion". 
  You'll be using Applitools to find and report bugs and handle dynamic content using Applitools' visual AI.
  You'll be working in the `Hackathon_Activity.py` file. An example solution is available in the `Hackathon_Solution.py`. 
  Don't look unless you're stuck! If you want to see view the expected results, you can run  `python hackathon_solution.py`.

1. Open up the `hackathon_activity` python file. Put your name (or team name) as the Batch name, and be sure to set your API key as you did in the first example. You can run this using `python hackathon_activity.py`.


2. We'll start with a test on [Applifashion V1](https://demo.applitools.com/gridHackathonV1.html). Create an Applitools test that navigates to the main page and takes a full page screenshot. See the first example on how to do this.

   
3. Next, we'll use the Cypress webdriver to click the "black" filter button, and then click the filter button. The needed CSS selectors are provided for your use. After filtering, take another screenshot with Applitools. 
   Both of these eyes.check calls should be within the same test.
   

4. Now, you'll use Cypress to click the "Appli Air x Night" shoes and take another full page Applitools check. You should have a test with 3 checks. 
 

5. Set the `dynamicContent` boolean to `true`. Re-run your test, and notice that your initial test will fail due to dynamic content. 
Draw a layout region over the area, or set the match level to "Layout" from within the SDK. Once you see that your test now passes, you can delete the region and turn off `dynamicContent`. 
   
 
6. Next, run the same test on the [Applifashion dev site](https://demo.applitools.com/tlcHackathonDev.html). To do this, change the `ENV_URL` to `APPLIFASHION_DEV`. Note that the main page doesn't have a shoe in the main area. 
   See that the black shoes filtering has a functional bug! Also notice how the "Appli Air x night" has a visual bug. 
   Place a bug region on each of the areas and accept the differences. Snooze failures on the bug regions for 2 weeks.
   

7. Development has made the changes to the bug region, which are on [Applifashion V2](https://demo.applitools.com/gridHackathonV2.html). 
Run your test suite on Applifashion V2 (Set `ENV_URL` to `APPLIFASHIONV2)
and accept the now-fixed change and delete the bug region. 
You'll see several unresolved tests; accept them and add or remove regions as needed!
  
 
8. You now want to test your site on multiple browsers and viewport sizes, including mobile viewports. Set the browser configurations in the eyes.configure "do" block. 
Add `iPhone_X` in portrait mode, and FireFox 1200 x 800 as browsers for the Ultrafast test cloud. Run the test to see your test 
   on these configurations!

### Additional Challenges
* Add another check that clicks the "Applifashion" home link in the upper left. What happens on v1 vs the dev environment? 


* Find a selector and apply a [coded region](https://help.applitools.com/hc/en-us/articles/360007188211-Coded-Ignore-Regions) to it. 

* Use the Applitools [PDF tester](https://applitools.com/tutorials/pdf-forms.html#analyze-your-test-results) to test some of your own PDF files. 

* Try testing a different site of your choice. Look for ways to handle dynamic content and get stable tests.  

* If you need more challenges, ask your hackathon administrator!

## Resources
- [Applitools SDK Documentation](https://applitools.com/docs/api/eyes-sdk/index-gen/classindex-selenium-python_sdk4.html)
- [Applitools Best Practices](https://applitools.com/docs/topics/general-concepts/visual-test-best-practices.html)