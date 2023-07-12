# Service level objectives

With an understanding of what users want define:

- Service Level Indicators (SLIs) -- metrics that matter
- Service Level Objectives (SLOs) -- what values we want the metrics to have
- Service Level Agreements (SLAs) -- how we react if we can't provide them

## SLI

An indicator is **a carefully defined quantitative measure of some aspect of the level of service that is provided**.

Examples:
- request latency (how long it takes to respond)
- error rate (as a fraction of all requests)
- throughput (requests per second)
- availability (fraction of time the service is usable)


## SLO

An objective is **a target value or range of values that is measured by an SLI**.

Examples:

- $SLI \le target$
- $lower\;bound \le SLI \le upper\;bound$

**Choosing an appropriate SLO is complex**. Publishing SLOs to users sets expectations about how a service will perform.

## SLA

Agreements are explicit or implicit contracts with users that includes consequences of missing SLOs. SRE doesn’t typically create SLAs because they are tied to business decisions.
