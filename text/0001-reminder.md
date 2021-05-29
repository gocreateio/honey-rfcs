---

rfc pr: [#1](https://github.com/gocreateio/honey-rfcs/pull/1)  
tracking issue: https://github.com/gocreateio/honey-rfcs/issues/1
---

# Reminder
As a user, I want to request `honey` to manage my reminders for me.

## Working Backwards

### README

Now `honey` can help you with your reminders - scheduling, editing, showing, and removing reminders.
You can communicate with her with your telegram app by writing or just talking.
E.g.,
```
User: Set a reminder for 7 am tomorrow: Meditation.
User: For every morning also.

User: Reschedule my 7 am reminder to 10 am.

User: Snooze reminder.
```

### PRESS RELEASE

Today, GoCreate community, announced the Honey, 
AI-Powered Virtual Assistant for busy professionals, business owners or anyone who needs personal virtual assistant.

Just say 'honey' and ask her anything. She will listen, learn, and do her best to help with information or knowledge you need any time.

Now, she knows how to conduct a secretary job for you.
Just ask her, and she will set a reminder, reschedule, cancel, or snooze it.
You will never miss anything, because your personal secretary is there for you, 24/7.

"The Honey, she is growing, learning, and getting intelligent day by day. Now, she knows how to manage reminders! I am offloading my personal and professional reminders to her with conversation, like I am talking to a real close person!". Steffen, GoCreate community contributor.

You can easily meet with her over your Telegram app and start to use her services now.

"She is like my sister, I don't know what I would do without her. She is not like another app, she has a human connection, humor, emotion and understanding. Looking forward to seeing her new skills.". Naomi Morioka, customer.

To meet the Honey just follow the following [link]().

## FAQ

### What are we launching today?
The Honey is community driven AI-Powered virtual assistant for busy professionals, business owners or anyone who needs personal virtual assistant.
At this moment Honey has only one secretary kill - manage reminders for you.

### Why should I use this feature?
If you want to improve your productivity in personal and professional life then offload all reminders to her.
She will never miss or forgets anything from your reminders.

## Internal FAQ

> The goal of this section is to help decide if this RFC should be implemented.
> It should include answers to questions that the team is likely ask. Contrary
> to the rest of the RFC, answers should be written "from the present" and
> likely discuss design approach, implementation plans, alternative considered
> and other considerations that will help decide if this RFC should be
> implemented.

### Why are we doing this?
It is our first MVP, with simple Reminder Agent which allows us to validate our hypotheses related to AI-Powered Virtual Assistant.

### Why should we _not_ do this?
The downsides are infrastructure cost. At this moment, we cannot predict the infrastructure load and cost at the launch.

### What changes are required to enable this change?
![architecture](../images/0001-reminder.drawio.svg)
> Briefly describe the high-level design approach for implementing this feature.
>
> As appropriate, you can add an appendix with a more detailed design document.
>
> This is a good place to reference a prototype or proof of concept, which is
> highly recommended for most RFCs.

### Is this a breaking change?

> If the answer is no. Otherwise:
>
> Describe what ways did you consider to deliver this without breaking users?
>
> Make sure to include a `BREAKING CHANGE` clause under the CHANGELOG section with a description of the breaking
> changes and the migration path.

### What are the drawbacks of this solution?

> Describe any problems/risks that can be introduced if we implement this RFC.

### What alternative solutions did you consider?

> Briefly describe alternative approaches that you considered. If there are
> hairy details, include them in an appendix.

### What is the high level implementation plan?

> Describe your plan on how to deliver this feature from prototyping to GA.
> Especially think about how to "bake" it in the open and get constant feedback
> from users before you stabilize the APIs.
>
> If you have a project board with your implementation plan, this is a good
> place to link to it.

### Are there any open issues that need to be addressed later?

> Describe any major open issues that this RFC did not take into account. Once
> the RFC is approved, create GitHub issues for these issues and update this RFC
> of the project board with these issue IDs.

## Appendix

Feel free to add any number of appendices as you see fit. Appendices are expected to allow readers to dive deeper to
certain sections if they like. For example, you can include an appendix which describes the detailed design of an
algorithm and reference it from the FAQ.
