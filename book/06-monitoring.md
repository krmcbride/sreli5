# Monitoring distributed systems

**How do we define "monitoring"?**

Google:

> Collecting, processing, aggregating, and displaying real-time quantitative data about a system, such as query counts and types, error counts and types, processing times, and server lifetimes.

They further distinguish monitoring into two categories:

- White-box monitoring -- Metrics, APM, profiling, logs, etc, emitted from the service internals.
- Block-box monitoring -- Testing external behavior as users would see it

> Your monitoring system should address two questions: what’s broken, and why?

<details>
<summary>Monitoring vs Observability</summary>

#### So where does Observability fit in?

There are [many](https://www.ibm.com/cloud/blog/observability-vs-monitoring) [articles](https://www.crowdstrike.com/cybersecurity-101/observability/observability-vs-monitoring/) on the subject, but [according to wikipedia](https://en.wikipedia.org/wiki/Observability_(software)) observability is "the measure of how well internal states of a system can be inferred from knowledge of its external outputs".

Both observability and monitoring rely on what is typically referred to as the 3 pillars of observability -- logs, traces and metrics.  The main difference between them is their scope and what they aim to achieve:

- Monitoring uses telemetry to assess the health of a service. Monitors are reactive in that they are created with the knowledge of a potential of failure in a specific area of the system.  Monitors tell us that _something is broken_.
- Observability, and the pursuit thereof, is the quality of having a holistic view of a complex system. With robust observability we can be _proactive_.  When a monitor tells us something is broken, observability tooling can tell us why.

</details>

**Then what is an alert?**

Google:

> A notification intended to be read by a human and that is pushed to a system such as a bug or ticket queue, an email alias, or a pager. Respectively, these alerts are classified as tickets, email alerts, and pages.

## The Four Golden Signals

- Latency -- show slow?
- Throughput -- how much?
- Saturation -- how full?
- Errors -- how bad?
