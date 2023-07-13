# Monitoring distributed systems

**How do we define "monitoring"?**

Google:

> Collecting, processing, aggregating, and displaying real-time quantitative data about a system, such as query counts and types, error counts and types, processing times, and server lifetimes.

They further distinguish monitoring into two categories:

- White-box monitoring -- Metrics, APM, profiling, logs, etc, emitted from the service internals.
- Block-box monitoring -- Testing external behavior as users would see it

> Your monitoring system should address two questions: what’s broken, and why?

<details>
<summary>Observability</summary>

#### So where does Observability fit in?

There are [many](https://www.ibm.com/cloud/blog/observability-vs-monitoring) [articles](https://www.crowdstrike.com/cybersecurity-101/observability/observability-vs-monitoring/) on the subject, but in the simplest terms, observability the degree to which an org is doing what google calls "white-box monitoring" -- the measure of how well internal states of a system can be inferred from knowledge of its external outputs.

Both observability and monitoring rely on what is typically referred to as the 3 pillars of observability -- logs, traces and metrics.  The main difference between them is their scope and what they aim to achieve:

- Monitoring uses telemetry to assess the health of a service.
- Observability aims to make complex systems observable via this telemetry so as to understand the behavior of the system as a whole (which greatly assists in the creation of good monitors). It supports what google calls "tools for post hoc analysis".

To go back to Google's monitoring definition: monitors tell you what's broken, observability can tell you why. Or put another way, you monitor symptoms, observability helps uncover the "why".

</details>


**Then what is an alert?**

Google:

> A notification intended to be read by a human and that is pushed to a system such as a bug or ticket queue, an email alias, or a pager. Respectively, these alerts are classified as tickets, email alerts, and pages.