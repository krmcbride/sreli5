# SRE vs DevOps

```typescript
interface DevOps {
  disableSilos(): void;
  getSystemFailures(): Metrics; // Accidents are normal, measurement is crucial
  doIncrementalBuild(): void; //  Change should be gradual
}

class SRE implements DevOps {
  doOps(approach: Software): void; // doing operations well is a software problem
  configureSLO(sli: SLI[]): void; // 100% reliability is not the goal, error budgets
  minimizeToil(toAutomate: Toil): void; // toil is not the job (50% or less), automate this year's job away
  reduceCostOfFailure(mttr: MeanTimeToRepair): void; // proactively uncover problems
  unifyTooling(): void; // SRE and product teams should use the same tools
  disableSilos(): void; // @override -- embed with and blur the lines with product developers, shared ownership
}
```

<details>
<summary>Team Topologies</summary>

### Where does SRE live in the [Team Topologies](https://teamtopologies.com/key-concepts) model?

Likely a combination of:

- Enabling team: helps a Stream-aligned team to overcome obstacles. Also detects missing capabilities.
- Platform team: a grouping of other team types that provide a compelling internal product to accelerate delivery by Stream-aligned teams

The common thread being that enabling and platform teams remove impediments to stream-aligned team agility.

#### And for reference, what is a steam-aligned team?

- stream-aligned team: aligned to a flow of work from (usually) a segment of the business domain

</details>