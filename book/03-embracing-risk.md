# Embracing risk

**Extreme reliability comes at a cost**. A user on a 99% reliable smartphone cannot tell the difference between 99.99% and 99.999% service reliability, because the user experience is dominated by less reliable components.


## Managing risk

Manage reliability by managing risk, conceptualize risk as a continuum. Of equal importance:
  - **engineering** greater **reliability**
  - **identifying** reliability **tolerance**.
  
## Measuring service risk

Usually the focus is "nines" (99.99% availability), eg "unplanned downtime", but its better to define availability in terms of **request success rate**.

$$
aggregate\;availability = \frac{successful\;requests}{total\;requests}
$$

> How to think about this: 1M req/day with availability target of 99.95% can serve up to 500 errors a day.

- Not all requests are equal (new user sign-up vs polling for something in the background)
- A batch system my think of "request" as job runs or number of records processed.
- Set quarterly availability targets for a service and track performance on a weekly, or even daily, basis (see SLOs).


## Risk tolerance of services

**SREs and product owners turn business goals into explicit engineering objectives**

#### Identifying risk tolerance

- What level of availability is required?
- Do different types of failures have different effects on the service?
- How can we use the service cost to help locate a service on the risk continuum?
- What other service metrics are important to take into account?

#### Identifying target level of availability

- What level of service do users expect?
- Does the service tie directly to revenue?
- Is the service paid or free?
- What level of service do competitors provide?
- Is the service targeted at consumers or at enterprises?

#### Types of failures

The expected shape of failures for a given service is another important consideration.

- How resilient is our business to service downtime?
- Which is worse for the service
  - a constant low rate of failures
  - an occasional full-site outage

Both types of failure may result in the same absolute number of errors, but may have vastly different impacts on the business.

#### Cost considerations

- If we achieve one more nine what would the incremental increase in revenue be?
- Does this revenue offset the cost of reaching that level of reliability?

## Error budgets

Product development performance evaluated on velocity, SRE performance is evaluated on reliability of a service. Creates tension with regard to:

- How hardened do we make the software to unexpected events
- Too much vs too little testing
- Frequency of deployments, canary design.

To base decisions on data, jointly define a quarterly error budget based on the service’s SLO. This is an objective metric that determines **how unreliable the service is allowed to be** within a single quarter.

Steps:

1. Product Management defines SLOs
2. Actual uptime is measured by a monitoring system
3. The difference between these two numbers is the "budget" of how much "unreliability" is remaining for the quarter.
4. As long as there is error budget remaining new releases can be pushed.

If SLO violations expend the error budget, releases are temporarily halted, slowed or rolled back while additional resources are invested in testing/development/resiliency/performance, etc.

**The error budget provides a common incentive that allows both product development and SRE to find a balance between innovation and reliability**.

The budget also highlights costs of overly high reliability -- if a team is having trouble launching new features, they may **loosen the SLO (increase the error budget) to increase innovation**.
