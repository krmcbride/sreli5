# Service level objectives

With an understanding of what users want define:

- Service Level Indicators (SLIs) -- metrics that matter
- Service Level Objectives (SLOs) -- what values we want the metrics to have
- Service Level Agreements (SLAs) -- how we react if we can't provide them

### SLI

An indicator is **a carefully defined quantitative measure of some aspect of the level of service that is provided**.

Examples:
- request latency (how long it takes to respond)
- error rate (as a fraction of all requests)
- throughput (requests per second)
- availability (fraction of time the service is usable)


### SLO

An objective is **a target value or range of values that is measured by an SLI**.

Examples:

- $SLI \le target$
- $lower\;bound \le SLI \le upper\;bound$

**Choosing an appropriate SLO is complex**. Publishing SLOs to users sets expectations about how a service will perform.

### SLA

Agreements are explicit or implicit contracts with users that includes consequences of missing SLOs. SRE doesn’t typically create SLAs because they are tied to business decisions.

## Indicators in practice

**What Do You and Your Users Care About?**

- Don't use every metric in your monitoring system as an SLI
- Too many indicators produces too much noise
- Too few may leave systems unexamined
- A handful of indicators are enough to evaluate and reason about a system’s health

Broad indicator categories:

- frontend/UI - availability, latency, throughput. 
- storage - latency, availability, durability. 
- data pipelines - data throughput, end-to-end latency (or focused on stages)
- all - correctness (was the right thing done?)

### Indicator collection

- Server side
  - Prometheus
  - Log analysis
- Client side
  - RUM
  - Sentry

**Metrics aggregation needs to be done carefully**.  Requests **per second** implicitly aggreagtes data over a window -- is the data sampled every second or minute?

> Consider a system that serves 200 requests/s in even-numbered seconds, and 0 in the others. It has the same average load as one that serves a constant 100 requests/s, but has an instantaneous load that is twice as large as the average one. Similarly, averaging request latencies may seem attractive, but obscures an important detail: it’s entirely possible for most of the requests to be fast, but for a long tail of requests to be much, much slower.

Most metrics are better as distributions than averages -- use percentiles to understand the shape of the distribution:
- A high-order percentile, such as the 99th or 99.9th, shows worst-case values
- 50th percentile (median) emphasizes the typical case. 

Strategies:
- focus on worst-case percentiles
- standardize indicator definitions, eg intervals, frequency.

## Objectives in practice

An example that takes the shape of a performance curve and variations in workload into consideration:

```
• 90.0% of requests will complete in <1ms
• 99.0% of requests with payload <1KB will complete in <10ms
• 99.9% of requests with payload <1KB will complete in <100ms
```

### Choosing targets

Not purely technical because the business should be reflected in the SLI/SLO/SLA. 

- Don't lock yourself into unrealistic expectations by basing a target on current performance.
- Keep it simple -- complex SLIs are hard to reason about.
- Less is more -- choose just enough SLOs to provide good coverage of the system. 
- Better to start with a loose target than a strict one -- refine SLOs as you learn

> Defend the SLOs you pick: if you can’t ever win a conversation about priorities by quoting a particular SLO, it’s probably not worth having that SLO. SLOs can—and should—be a major driver in prioritizing work for SREs and product developers, because they reflect what users care about. A good SLO is a helpful, legitimate forcing function for a development team. Using tighter internal SLOs than the SLO advertised to users gives you room to respond to chronic problems before they become visible externally.

