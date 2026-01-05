# Bot-Detection-Task

## Introduction

When Looking at a recent surge of unusual traffic on website. There is always a suspicion of the bot activity on the website but we cannot block all of the suspicious looking requests to our servers because it may lead to losing our original or organic human traffic but not doing anything about this would also mean exposing our website or server to the bots.

So as per my approach we need to find middle grounds for this purpose of tackling this issue such that we only block bots and not restrict the real users from accessing the servers or our website. For this purpose we would need to keep an eye on the "digital Footprints" left by the bots when they use a server or make request to a server following these we can filter out bots among the real users, So i have outlined some of the indicators of bot activity and measures we could take to avoid them.


## 1. Indicators of Bot Activity

* Request Patterns and Frequency - 
  * Humans have physical limit to make a limited number of requests per minute surpassing that limit to a large extent could be a possible indicator of the suspicious bot activity on the server or website.
  * Humans cannot make requests at a continuous time interval in such a small time duration consistently hence this is the possible indicator of a automated script being used to make the requests.
  * Unusually high traffic on the server or website during odd hours.

* Behaviour of Sessions -
   * Unusually short session durations with many actions completed in an instant on the server.
   * Repeated activity or workflow on the server
   * Sessions with unusual or no mouse activity and key movements.
   * A normal human would always go on homepage first then move to some other related pages bots often know the website and move directly to endpoints without visiting homepage.
 
* Input Patterns
  * Humans have often a curved mouse pattern when surfing or scrolling a site whereas bots dont have these.
  * Humans have a varied keystroke timings whereas bots have unusually a similar pattern or interval in thier keystrokes focusing no delay from thier previous keystroke.
  * Bots paste massive amounts of textx in the form instantly.

## 2. Detection Methods

* Requests based detections -
  * Limit the rate of requests per IP/session or implement a per minute rate limit to avoid misuse by the bots.
  * Flag the IP's that make unusually large amounts of requests and mark them suspicious or restrict them from server or temprory block.
  * Monitor the IP's that are making requets during the odd hours and block them temprorily.
 
* Behavioural based Analysis -
  * Track Mouose movements and key stroke timings and scrolling.
  * Measure the randomness in these as compared to that of humans.
  * Scripts/Bots have a predictable movement pattern or time interval.

* HoneyPot Input Fields -
  * As the bots only read the html of the page make a hidden input field which only bots are able to see and not accesible to humans make it not compulsory field if the bot fills that field its automatically          detected as the bot session since a normal human would never have been able to see that field.

* Session Timing Based Detection -
  * If a unusually short time has been spent in a session and lots of work or pages have been accesed during that time we can flag it as a suspicious bot activity.
  * if the session has directly started on some other page rather than home its possible indicator of bot activity however this could also be due to browser cookies hence no confirmation but we can flag this.
 

