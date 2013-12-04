---
layout: post
title:  "Starting Ruby Style Guide - notes"
date:   2013-12-04 19:10:29
tags: ruby styleguide
---

Despite my best intentions **Sublime Text 2** deceived me. 
As a result my code didn't follow the most basic [Ruby Style Guideline](https://github.com/bbatsov/ruby-style-guide "Ruby Style Guideline"), 2 spaced indents.

*So what went wrong?*

Sublime showed me **2 spaced indentation** like this:
{% highlight ruby %}
def create_deck
  suits = %w(Hearts Diamonds Spades Clubs)
  cards = %w(2 3 4 5 6 7 8 9 10 Jack Queen King Ace)
  deck = []
  5.times do # using 5 decks
    deck += suits.product(cards)
  end
  deck
end
{% endhighlight %}

Upon review in Github my code looked like this, note the **large tabbed indentation**:

{% highlight ruby %}
def create_deck
		suits = %w(Hearts Diamonds Spades Clubs)
		cards = %w(2 3 4 5 6 7 8 9 10 Jack Queen King Ace)
		deck = []
		5.times do # using 5 decks
				deck += suits.product(cards)
		end
		deck
end
{% endhighlight %}
<br>
**To fix this in Sublime Text.**

	1.	Select all your code (CTRL-A)
	2.	Click "Space: x" in the bottom bar of Sublime
	3.	Select "Convert Indentation to Spaces"
	4.	Save your file
<br>
**To fix a file already on github** (without pushing it through again)

	1.	Navigate to your code's repository
	2.	Open the file by clicking on it
	3.	Click 'Edit' at the options above your code
	4.	Click the drop-down box above the code that says 'Tabs'
	5.	Change it to spaces
	6.	Commit the changes at the bottom of the page.