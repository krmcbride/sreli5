# SRE intro

SREs main categories:

- 50–60% are SWE
- 40–50% are very close to SWE qualifications but have additional skills, usually UNIX system internals and networking (Layer 1 to Layer 3).

### It is crucial that SRE teams are focused on engineering

Ops teams cannot scale linearly with the size of the workload 

- Google places a 50% cap on the aggregate "ops" work for all SREs—tickets, on-call, manual tasks, etc. 
- Google’s rule of thumb is that an SRE team must spend the remaining 50% of its time actually doing development.

SRE teams being focused on engineering allows them to scale sublinearly with workload size.

### 100% is the wrong reliability target for a system

A service that’s 99.99% available is 0.01% unavailable. That permitted 0.01% unavailability is the service’s error budget. We can spend the budget on anything we want, as long as we don’t overspend it.

### Monitoring should never require a human to interpret any part of the alerting domain

Software should do the interpreting, humans should be notified only when they need to take action.

Three kinds of monitoring output:

- Alerts: Signify that a human needs to take action immediately in response to something that is either happening or about to happen
- Tickets: Signify that a human needs to take action, but not immediately. The system cannot automatically handle the situation, but if a human takes action in a few days, no damage will result.
- Logging: No one needs to look at this information, but it is recorded for diagnostic or forensic purposes. The expectation is that no one reads logs unless something else prompts them to do so.

### Reliability is a function of mean time to failure (MTTF) and mean time to repair (MTTR)

Having on-call runbooks is 3x better MTTR than just winging it.

### 70% of outages are due to changes in a live system

Change management best practices:

- Implement progressive rollouts
- Quickly and accurately detecting problems
- Roll back changes safely when problems arise