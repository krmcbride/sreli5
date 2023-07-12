# Eliminating toil

We want to be focused on long-term engineering work, not toil. What is toil?

Google defines toil as work that is:

- manual: e.g. manually running scripts
- repetitive: same work done over and over
- automatable: if a machine could do it just as easily, eg does not require human judgement
- tactical: i.e. reactive, not proactive. Handling pager alerts is toil.
- has no enduring value: i.e. the work does not produce a permanent improvement
- scales linearly with service growth

**The work of reducing toil and scaling up services is the "engineering" in SRE**.

> Engineering work is what enables the SRE organization to scale up sublinearly with service size and to manage services more efficiently than either a pure Dev team or a pure Ops team. Engineering work is novel and intrinsically requires human judgment. It produces a permanent improvement in your service, and is guided by a strategy. It is frequently creative and innovative, taking a design-driven approach to solving a problem—the more generalized, the better. Engineering work helps your team or the SRE organization handle a larger service, or more services, with the same level of staffing.

SRE activities:

- Software engineering - writing code, e.g. automation scripts, internal frameworks, improving service scalability/reliability, improving infra-as-code.
- Systems engineering - improving system configuration and documenting systems in a way that produces lasting benefits, i.e. monitoring setup, load balancing, OS tuning, consulting on architecture and production readiness.
- Toil - (see above)
- Overhead - administrative work (HR, meetings, assessments)