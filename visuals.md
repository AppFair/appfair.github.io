App Fair Process Visuals
========================

## Intro

```mermaid
flowchart LR
    A(Create App) -- Design\nBuild\nDocument\nTest --> B(Prepare\nRelease)
    B -- Submit\nPull\nRequest --> C{{TRUSTED\nreplication\nautomation}}
    B -- Create\nRelease --> D(UNTRUSTED\nbuild\nautomation)
    D -- App.ipa --> E
    C -- App.ipa --> E{Verify\nScan\nIndex\nSeal}
    E -- assemble\ncatalog --> Publish
```

