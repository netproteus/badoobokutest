# badoobokutest

This mocks up a payment integration between badoo and boku and what happens on the return to badoo on the competion of payment

The code in boku.html closely follows the actual code used for this step in https://buy2.boku.com/ui/static/1.33.0/scripts/checkout.js
and where the problem is located

You can see a live example here http://netproteus.com/boku-test/badoo.html

And two possible solutions in order of preference

1. Stop trying to do anything with window.opener.location, redirecting our parent page is never what we want.
https://github.com/netproteus/badoobokutest/pull/1

2. Tell us how to configure the orgrl controller parameter so your code will actually post a message to our parent (this will require hacking on our part and we would definitely prefer you just redirected the popup window to the url we asked you to.
https://github.com/netproteus/badoobokutest/pull/2
