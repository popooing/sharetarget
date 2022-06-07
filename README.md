# sharetarget

https://github.com/boss12123/flexmessage

Example static web file to use feature shareTargetPicker api (integrate with LIFF), Can be used in many places, such as Flex message, Rich menu.

screenshot.gif

Features!
Customs share dynamic messages from query url.
Use parameter in your messages to replace with user data from LINE.
Compatible with both on LINE application and external browser.
Usage
You just copy only index.html file and place to some static web host, such as GitHub Pages.

Create you messages to share, such as flex message, follow at liff.shareTargetPicker() or get example data in exampleFlexMessages.json.

options: use parameter for replace your messages with data from line

Put your messages file or api to somewhere host, you can quick try on some free service like mocki.io or create file on github as well.

Create LIFF and enter full url of index.html is placed and along with query params with value from the above steps to Endpoint URL setting. e.g. value in Endpoint URL

https://mysite.com/sharetarget/index.html?liffId=1234-abcd&messages=https://mysite.com/messages.json
Try to enter LIFF url is created on Line App such as, Text Message, Flex message, Rich menu to view result. 👍

PS. You can split messages query params on Endpoint URL and place it after LIFF URL. e.g.

https://liff.line.me/1234-abcd?messages=https://mysite.com/messages.json
Demo
You can try with this resouce.

app url:

https://tues.cc/line/shareTargetPicker

messages url (it's flex with use parameter):

https://tues.cc/line/shareTargetPicker/exampleFlexMessages.json

or my result LIFF Url:

https://liff.line.me/1654395981-1Enp60g8?messages=https://tues.cc/line/shareTargetPicker/exampleFlexMessages.json
Query Params:
Name	Require	Description
liffId	yes	LIFF ID e.g. 1234-abcd.
messages	yes	Url of json messages file or api.
Options
Messages Parameter
use e.g. {{parameterKey}} place to somewhare on your messages will replace by data from line.

Key	Description
profile.key	Can access all key and return follow liff.getProfile() displayName pictureUrl statusMessage userId, e.g. {{profile.displayName}}
shareThis	Return current LIFF url and all query params e.g. {{shareThis}}
