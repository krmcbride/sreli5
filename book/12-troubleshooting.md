# Troubleshooting

## Triage

Your first instinct may be to troubleshoot and find a cause -- ignore that instinct!

**Your course of action should be to make the system work as well as it can under the circumstances.**

- Divert traffic
- Drop traffic
- Disable a subsystem
- Etc

Stop the bleeding.

> Novice pilots are taught that their first responsibility in an emergency is to fly the airplane; troubleshooting is secondary to getting the plane and everyone on it safely onto the ground


## Examine

Once the bleeding is stopped, use all available observability tooling to determine what's behaving and what isn't.

## Diagnose

**Simplify and reduce** -- look at connections between components to determine what is working and what isn't. Interacting with components using known test data can be particularly helpful.

It can be helpful to start at the "beginning" of a pipeline and examine each stage, or split the system in half and examine communication on each side.

> A malfunctioning system is often still trying to do **something** — just not the thing you want it to be doing.
> 
> Finding out **what** it’s doing, then asking **why** it’s doing that and **where** its resources are being used or where its output is going can help you understand how things have gone wrong

**What touched it last? Systems have inertia -- systems tend to remain in motion until acted upon by an external force.**


todo: negative results, test and treat