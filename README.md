
```{mermaid}
%%| label: fig-mermaid-flowchart
%%| fig-cap: Wow look how it flows.

graph LR
    A([Oooh]) --> B([Would You])
    B --> C([Look at This])
    C --> D[Very]
    C --> E[Fancy]
    C --> F[Flowchart]
```

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

```mermaid
flowchart TD;
    setup-dev((Setup))
    bci{{Build Container Image}}
    click bci "vfarcic/cncf-demo/blob/main/manuscript/build-container-imge/story.md" _blank
    style bci fill:red

    bci-lima(Lima)
    bci-buildpacks(Cloud Native Buildpacks / CNB)
    bci-kbld(Carvel kbld)

    setup-dev-->bci
    bci-->bci-lima-->registry
    bci-->bci-buildpacks-->registry
    bci-->bci-kbld-->registry

    registry{{Store Contnr Img In Reg}}
    style registry fill:yellow
```
