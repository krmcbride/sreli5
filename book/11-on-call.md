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

Aim to have **no more than 25% of an SRE's time on-call**. Using this approach and assuming a primary and secondary with week-long shifts, the minimum number of SREs is 8 for 24/7 coverage. A _follow the sun_ rotation is ideal to prevent night shifts.

SREs should have sufficient time to not only deal with incidents but complete postmortems.

### Feeling safe

Reducing on-call stress is essential. The most important on-call resources are:

- Clear escalation paths
- Well-defined incident-management procedures
- A blameless postmortem culture

Dev teams of SRE-supported systems participate in on-call rotation, and are available for escalation.

<details>
<summary>Blameless and a Just Culture</summary>

From https://www.etsy.com/codeascraft/blameless-postmortems/

> Having a Just Culture means that you’re making effort to balance safety and accountability. It means that by investigating mistakes in a way that focuses on the situational aspects of a failure’s mechanism and the decision-making process of individuals proximate to the failure, an organization can come out safer than it would normally be if it had simply punished the actors involved as a remediation.
>
> Having a “blameless” Post-Mortem process means that engineers whose actions have contributed to an accident can give a detailed account of:
>
> - what actions they took at what time,
> - what effects they observed,
> - expectations they had,
> - assumptions they had made,
> - and their understanding of timeline of events as they occurred.
>
>...and that they can give this detailed account without fear of punishment or retribution.

</details>