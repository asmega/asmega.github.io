---
layout: post
title: How to import into reminders for ios and mac
date: 2019-10-11 20:00
summary: A semi-automated process
categories: "mac ios reminders how-to import migrate apple catalina"
---

Apple recently updated reminders for ios 13 and macos cataina. It's free, integrates with the apple ecosystem and has some fairly powerful features. It looked like it could replace my current todo app [TickTick](https://www.ticktick.com/) which I have a subscription for.

To get started though I'd have to migrate all my exisiting lists into reminders. There's no import functionality so a big pain for anyone wanting to switchover.

I managed to get some kind of script working to do basic migrations of my lists with [Automator](https://en.wikipedia.org/wiki/List_of_macOS_components#Automator) and [AppleScipt](https://en.wikipedia.org/wiki/AppleScript)

Below is the code you will need to be able to import todos into reminders for mac and ios

{% highlight applescript %}
set theList to {"buy milk", "defrost chicken", "watch netflix"}
repeat with a from 1 to length of theList
  set theCurrentListItem to item a of theList
  tell application "Reminders"
    tell list "inbox" of default account
      make new reminder with properties {name:theCurrentListItem}
    end tell
  end tell
end repeat
{% endhighlight %}

Most other todo apps will allow you to export to CSV or other formats. However AppleScript seems awful at handling CSVs. I recommend converting all your todos into the format above in a text editor then run it in Automator.
