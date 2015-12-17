QVSource Twitter Starter App Pack For QlikView
==============================================
This is a starter QlikView application pack showing how to get started using the [QVSource Twitter Connector](http://wiki.qvsource.com/Twitter-Connector-For-QlikView.ashx) for QlikView.

*Note that the [load script](https://github.com/QVSource/QVSource-Twitter-Starter-App-For-QlikView/blob/master/Twitter-Starter-App-Load-Script-And-Data-Model-Alternative-UI-prj/LoadScript.txt) should also work in Qlik Sense.*

Full documentation for this starter application can be found [here](http://wiki.qvsource.com/Twitter-Tracker-Demo-Application-For-QlikView.ashx).

It also makes use of the [Sentiment and Text Analytics Connector](http://wiki.qvsource.com/Sentiment-Analysis-And-Text-Analytics-Connector-For-QlikView.ashx) to score Tweets and the [Klout Connector](http://wiki.qvsource.com/Klout-Connector-for-QlikView-%28v2%29.ashx) to measure the influence of Tweeters.

If you are a QlikView (or Qlik Sense) + QVSource user you can simply click the ["Download ZIP"](https://github.com/QVSource/QVSource-Twitter-Starter-App-For-QlikView/archive/master.zip) button on GitHub to grab this application.

The content below is copied from the change log in the first tab of the load script.

Change Log
==========
1.0.9.0 - 17/12/15
------------------
* Made change outlined here [http://wiki.qvsource.com/Upgrading-to-version-1_1-of-the-Sentiment-Analysis-And-Text-Analytics-Connector.ashx] to make app compatible with QVSource Web Editios and QVSource WinForms Edition 1.6.7.0 and later.

1.0.8.3 - 04/12/13
------------------
* Updated badge.

1.0.8.2 - 29/08/13
------------------
* maxCacheAgeInHours parameter for UserLookup table changed from -1 (cache indefinitely) to 1 (hour).

1.0.8.1 - 30/07/13
------------------
* Added check that vLocalTimeZone is recognised.
* Moved to Github.

1.0.8 - 25/06/13
----------------
* BREAKING CHANGES - You will not be able to simply start reloading this over the top of QVDs created from earlier versions.
* Fixed issue where searchmaxpages in Params table should be maxNoPages
* Removed RT and -RT as separate searches - this is now worked out from the presence/absence of a rewteeted status.
* Added a Search_IsReply field (true/false).
* Added a lot more fields to the search results table (and QVD) but only loading in a small subset of these. Feel free to uncomment more fields in the LoadFromQVDs table.
* loadFromQVDs is now in a sub and called from Main.
* Reply added as a TweetType and a new Search_IsRetweet field added if you just want to distinguish Tweets and Retweets.
* Added show condition and message for keyword lookup.
* Added a second tab where we are sketching out some ideas for new charts.
* Added frequency to some list boxes.

