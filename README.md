# Clojurians Slack Log demo data

This is a small subset of the raw logging data that is gathered from the
Clojurians Slack community. It is here to help people who want to help improve
the app that displays these logs, found at
[clojureverse/clojurians-log-app](https://github.com/clojureverse/clojurians-log-app).
You can find instructions on what to do with this data over there.

What you find here is the data from the first 9 days of February 2018, as well
as the data of users and channels that were active during this period.

This is "real" data, with two differences

- user email addresses have been replaced with fakes
- message text that has been deleted or changed has been scrubbed

## Why don't you just make the raw logs public?

We've considered this. People should assume that what they post on Slack is
public, so this should be fine, but there are a few reasons why we chose not to
do this.

A person with bad intentions could use this data to specifically filter and
search through the chat history of a single person, looking either for
identifying or incriminating information. This is the main threat model we
consider. The website with the logs is still public, so a persistent individual
could still do this, but we're not making it trivial.

Slack allows people to edit or delete messages. In these cases we only display
(or don't display) the end result. The original message and the change events
are all present in the raw log data though, and so we choose not to share those.
That is also why the data in this repo has been processed, to remove such events.

Finally, if a user asks to remove their message history from the archive then we
must honor that. This would be near impossible if the complete history is a git
repo that anyone can clone.
