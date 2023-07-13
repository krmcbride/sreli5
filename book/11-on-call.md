# Being on-call

> As the **guardians of production systems**, on-call engineers take care of their assigned operations by managing outages that affect the team and performing and/or vetting production changes.

The expected paging response times may differ depending on the kind of page. When a page is acknowledged the engineer is expected to triage work toward a resolution, escalating as needed.

Many teams have both a primary and a secondary on-call rotation, or the another team's on-call can serve as a secondary.

Lower priority alerts can be handled by the on-call engineer during business hours.

<details>
<summary>Dealing with interrupts</summary>

Categories of "operational load":

- Pages concern production alerts and are triggered in response to production emergencies. Pages always have an expected response time (SLO), which is sometimes measured in minutes.
- Tickets concern customer requests that require you to take an action. Like pages, tickets can be either simple and boring, or require real thought. Tickets may also have an SLO, but response time is more likely measured in hours, days, or weeks.
- Ongoing operational responsibilities (also known as "Kicking the can down the road" and "toil") like responses to ad hoc, time-sensitive questions from customers. While they may not have a defined SLO, these tasks can interrupt you.

**Flow state**, or being in "the zone", can increase productivity and creativity. Being interrupted kicks you out of this state.

While on-call, if focusing on interrupts, **interrupts stop being interrupts**. When you're doing interrupts your projects become a **distraction**.

### Distractibility

In order to limit your distractibility, you should try to minimize context switches. Assign a cost to context switches. **Polarizing time** means that when a person comes into work each day, they should know if they’re doing _just_ project work or _just_ interrupts.

</details>