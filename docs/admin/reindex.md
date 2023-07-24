---
sidebar_position: 4
---

# Reindex
Build the Bedework index, look at list of index, point to new index.

1.	Log in to Events JMX (hawtio) or Steven JMX (hawtio).
    1. [https://events.library.nashville.org/hawtio/login](https://events.library.nashville.org/hawtio/login)
    1. [https://steven.library.nashville.org/hawtio/login](https://steven.library.nashville.org/hawtio/login)
1.	Click `JMX` in the horizontal menu.
1.	Click on `org.bedework.bwengine`
1.	Click on `indexing` in the left menu
1.	Click Operations in the top menu
1.	Scroll down to bottom and find `rebuildIndex()`
1.	Click green Execute button
1.	When you get the list of indexes, copy (or jot down) the latest index. Will look something like: `bwuserp20190402t114137`
1.	Click on Close button
1.	Now you have to point to the new index you just built. Go to `setProdAlias(java.lang.String)`.
1.	You should see a text box with P1 next to it. Paste in that text into the box.
1.	Click `Execute` button.
1.	If you see OK, click on `Close` button.
1.	Go to `listIndexes()`
1.	Click `Execute` button.
1.	Make sure you advanced the pointer to the most recent index.
1.	You can click on `rebuildStatus()` to check on progress. Same series of steps: Execute, Close. At the end, you will get a message that says something like “index complete.” Usually takes around 10-15 mins.
