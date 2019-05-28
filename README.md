# grove-test
NS programming test for Grove Collaborative

Notes on grove collaborative coding challenge:
Nodejs would be more fun, but if this is a netsuite developer position, I want to code it in Suitescript.
I am starting this late on monday, so since I'm faster with SuiteScript 1, am doing it in SS1. Converting ss1 to ss2 is still easier for me at this point. I want to be doing all my projects in SS2.

Using a suitelet that would need to be uploaded as a script, configured (for example, in the deployment, add it to the "classic" center transaction and then this will appear in a NetSuite menu as a link under transactions -> custom -> <deployment title>. Use function "gAddressPage". Then a NetSuite employee could navigate to this page to find a store - they wouldn't be limited to using the computer that the command line is installed on, of course.

I took a very brief look online for the very relevant challenge of parsing a free form address, a bane of many data systems. With node, I would have invariably at least tried modules that have the most up-to-date support, and widest user base. However, with cloud solutions, I like to rely on managed software first rather than manually managed functions/utilities (ie that need its codebased updated periodically) unless it doesn't make sense architecturally. I chose smartystreets.com for a location, mainly because they're free for 250 requests/month, and are scalable. There are many services available for this that could be further researched.

Other concessions and area of further research would be the CSV parsing - stress testing with with special characters, missing data etc etc, and doing more spot tests with different addresses. Papaparse looked to have a relatively good backing behind it. There may be even better tools out there for that particular job.
Note that I uploaded the file into the NetSuite file cabinet. Another method for this would be to convert the csv into records and utilize a saved search to grab the rows, which would make sense if the list of locations would be actively managed in NetSuite.

technical notes:
I need to do a lot of cleanup - pass object not string parameters, error catching decisions, change zip/object formatting to gAddressPage function rather than the form rendering function, other minor cleanup. Note the version is 0.4. Working but not at all stress tested. 
