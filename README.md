graph TD
    subgraph Office Layout
        MW[Mwape's Desk]
        C1[Chair 1 (Tasila)]
        C2[Chair 2 (Mutinta)]
        W[Window (City View)]
        D[Door]
    end

    subgraph Cameras
        A(A-Cam: 24mm - Master/Group)
        B(B-Cam: 50mm - Dialogue/Medium)
        C(C-Cam: 50mm - Reaction/Tight)
    end

    style MW fill:#b0e0e6,stroke:#333,stroke-width:2px
    style C1 fill:#f5f5dc,stroke:#333,stroke-width:1px
    style C2 fill:#f5f5dc,stroke:#333,stroke-width:1px
    style W fill:#add8e6,stroke:#333,stroke-width:1px
    style D fill:#cccccc,stroke:#333,stroke-width:1px

    direction LR

    A -- "Medium 3-Shot" --> C1 & C2 & MW
    B -- "Tight Shot (Tasila/Mutinta)" --> C1 & C2
    C -- "Reaction (Mutinta/Tasila)" --> C2 & C1

    subgraph Initial Setup (Negotiation)
        direction LR
        A -- (Wide coverage of all 3) --> MW
        B -- (Closer on Tasila) --> C1
        C -- (Reaction shot on Mutinta) --> C2
    end

    subgraph Kisses Setup
        direction LR
        A(A-Cam: 24mm) --- "Mwape & Tasila (Kiss)"
        B(B-Cam: 50mm) --- "Tight ECU (Mwape & Tasila Kiss)"
        C(C-Cam: 50mm) --- "Reaction (Mutinta)"
    end
    Kisses Setup -. then switch C to Tasila for Mutinta's kiss .-> Kisses Setup2

    subgraph Kisses Setup2
        direction LR
        A(A-Cam: 24mm) --- "Mwape & Mutinta (Kiss)"
        B(B-Cam: 50mm) --- "Tight ECU (Mwape & Mutinta Kiss)"
        C(C-Cam: 50mm) --- "Reaction (Tasila)"
    end


    subgraph Scene 2 Plan
        MW -- Chair facing desk --> C1
        MW -- Chair facing desk --> C2

        A -. positioned wide, slightly off-axis from Mwape's POV .-> MW
        B -. focused on Tasila's initial aggressive lines .-> C1
        C -. focused on Mutinta's calculating reactions .-> C2

        A --(During Kisses)---> MW & C1 & C2 (maintains context)
        B --(During Kisses)---> C1 & MW (tight on specific kiss)
        C --(During Kisses)---> C2 (tight on reaction of *other* woman)
    end

    linkStyle 0 stroke-width:0px,fill:none;
    linkStyle 1 stroke-width:0px,fill:none;
    linkStyle 2 stroke-width:0px,fill:none;
    linkStyle 3 stroke-width:0px,fill:none;
    linkStyle 4 stroke-width:0px,fill:none;
