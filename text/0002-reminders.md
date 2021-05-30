---

rfc pr: [#1](https://github.com/gocreateio/honey-rfcs/pull/2)
tracking issue: https://github.com/gocreateio/honey-rfcs/issues/2
---

# Reminders

As an entrepreneur, I want `honey` to manage my routine tasks,
so I can focus on unblocking creativity and delivering business value.

## Working Backwards

### README

Now `honey` can help you with your reminders - scheduling, editing, showing, and removing reminders.
You can communicate with her with your telegram app by writing or just talking.
E.g.,

```
User: Set a reminder for 7 am tomorrow: Meditation.
User: For every morning also.

User: Reschedule my 7 am's reminder to 10 am.

User: Snooze reminder.
```

### PRESS RELEASE

Today, the GoCreate community announced the Honey, AI-Powered Virtual Assistant  
for young entrepreneurs who need productivity improvement with a personal virtual assistant.

Sometimes, it is not easy to balance life and work in startup life, especially for young entrepreneurs.
Having someone who can listen, assist, or advise is vital.
Even if someone is not a human but a digital, AI-powered assistant.
The assistant, who can automate your routine tasks, help you to unleash creativity and deliver business value.

Just say `honey` and ask her anything. She will listen, learn, and do her best to help with information or knowledge you need at any time.

Now, she knows how to conduct a secretary job for you.
Just ask her, and she will set a reminder, reschedule, cancel, or snooze it.
You will never miss anything, because your personal secretary is there for you, 24/7.

- "The Honey, she is growing, learning, and getting intelligent day by day.
  Now, she knows how to manage reminders!
  I am offloading my personal and professional reminders to her with a conversation like I am talking to a real close person!".
  Steffen, GoCreate community contributor.

You can easily meet with her over your Telegram app and start to use her services now.

- "She is like my sister; I don't know what I would do without her.
  She is not like another app; she has a human connection, humor, emotion, and understanding. Looking forward to seeing her new skills.".
  Naomi Morioka, the customer.

To meet the Honey, follow the following [link](https://t.me/gocreatehoneybot).

## FAQ

### What are we launching today?

The Honey is a community-driven AI-Powered virtual assistant for busy professionals, business owners, or anyone who needs a personal virtual assistant.
At this moment, Honey has only one secretary kill - manage reminders for you.

### Why should I use this feature?

If you want to improve productivity in your personal and professional life, then offload all reminders to her.
She will never miss or forgets anything from your reminders.

## Internal FAQ

### Why are we doing this?

With a simple Reminder Agent, our first MVP allows us to validate our hypotheses related to AI-Powered Virtual Assistants.

### Why should we _not_ do this?

The downside is infrastructure cost. At this moment, we cannot predict the infrastructure load and cost at the launch.

### What changes are required to enable this change?

![architecture](../images/0002-reminder.drawio.svg)

As shown in the figure above, a customer interacts with the Telegram app as a Telegram user via Telegram Bot.
Most of the heavy lifting is done by [Dialogflow] via [GCP]:

- Natural Language Processing
- Bot logic
- Cloud Function
- ML
- Cloud Storage
- Etc.
  Also, Prebuild Agents are part of [Dialogflow], which is extendable or can combine multiple agents into a single agent (i.e. [mega agent])

### Is this a breaking change?

No

### What are the drawbacks of this solution?

Also, it is not clear if we use [Google Assistant] as one of the channels.

### What alternative solutions did you consider?

[Google Assistant] can replace the need for the Telegram app and can a solo channel with its own pros and cons.

### What is the high-level implementation plan?

Please look at the [project board] for a detailed plan and deliver this feature from prototype to GA.

### Are there any open issues that need to be addressed later?

As it is our first MVP, we are in the stage of Unknown Unknowns.

## Appendix

> Feel free to add any number of appendices as you see fit. Appendices are expected to allow readers to dive deeper into
> certain sections if they like. For example, you can include an appendix that describes the detailed design of an
> algorithm and reference it from the FAQ.

[DialogFlow]: https://dialogflow.com/
[GCP]: https://cloud.google.com/
[Google Assistant]: https://assistant.google.com/
[mega agent]: https://cloud.google.com/dialogflow/es/docs/agents-mega
[project board]: https://github.com/gocreateio/honey/projects/1
