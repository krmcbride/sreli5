# Managing incidents

An _unmanaged incident_ is a shit show of people running around with their hair on fire and pointing fingers at each other. 

A process is all about communication, to prevent freelancing and focus the attention on stopping the bleeding.

### Recursive Separation of Responsibilities

- Make sure all involved know their role. Counterintuitively, a clear separation of responsibilities allows more autonomy
- If the load on someone becomes excessive they should delegate work to others, e.g. creating subincidents. A role leader might delegate system components to colleagues, who report high-level information back up to the leaders.

#### Distinct roles should be delegated

- Incident commander -- holds the high-level incident state, holds all positions until delegated.
- Ops lead -- applies operational tools to the task at hand. The only group modifying the system.
- Comms -- The public face of the incident response, issues periodic updates to stakeholders, may keep the **Incident State Document** up to date.
- Planning -- Assist ops with creation of tickets, arranging handoffs, tracking system divergence, etc.

It should be obvious where and what tool is used for communication, e.g. a known "war room" on Slack, Google meet, etc.

The **incident state document** ([example](https://sre.google/sre-book/incident-document/)) being updated is crucial so those joining the incident can get up to speed.

### When to Declare an Incident

**It is better to declare early and then find a simple fix than to spin up the incident management framework hours into a problem**.

Set clear conditions for declaring an incident. Some possible guidelines:

- Do you need to involve a second team in fixing the problem?
- Is the outage visible to customers?
- Is the issue unsolved even after an hour’s concentrated analysis?

Use the framework frequently, like as part of change management or DR, or simulate incidents.

### Best Practices for Incident Management

- Prioritize -- Stop the bleeding, restore service, and preserve the evidence for root-causing.
- Prepare -- Develop your incident management procedures in advance.
- Trust -- Give autonomy within the assigned role to all incident participants.
- Introspect -- Pay attention to your emotional state. If you start to feel overwhelmed solicit more support.
- Consider alternatives -- Periodically consider your options and re-evaluate whether it still makes sense to continue what you’re doing
- Practice -- Use the process routinely so it becomes second nature.
- Change it around -- Were you incident commander last time? Take on a different role this time. 

