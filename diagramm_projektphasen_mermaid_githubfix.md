# Projektphasen-Diagramm (Mermaid)

```mermaid
%%{init: {
  "theme": "neutral",
  "flowchart": { "nodeSpacing": 30, "rankSpacing": 35, "curve": "linear" }
}}%%

flowchart TB

classDef top fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.4px;
classDef bar fill:#ffffff,stroke:#000000,color:#000000,stroke-width:2px;
classDef soft fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.2px;
classDef txt fill:#ffffff,stroke:#000000,color:#000000,stroke-width:0.8px;
classDef ghost fill:transparent,stroke:transparent,color:transparent;

linkStyle default stroke:transparent;

%% obere Prozesskette
subgraph row1[" "]
direction LR
A["Bedarfs-<br/>definition"]:::top
B["Bedarfs-<br/>planung"]:::top
C["Projekt-<br/>entwicklung"]:::top
D["Planung"]:::top
E["Genehmi-<br/>gungs-<br/>planung"]:::top
F["Ausführungs-<br/>planung"]:::top
G["Auftrags-<br/>vergabe"]:::top
H["Realisierung"]:::top
I["Betriebs-<br/>übergang"]:::top
J["Betrieb"]:::top
end
style row1 fill:transparent,stroke:transparent
A --> B --> C --> D --> E --> F --> G --> H --> I --> J

%% Freigaben / Beschlüsse
subgraph row2[" "]
direction LR
A2[" "]:::ghost
B2["Anforderungs-<br/>freigabe"]:::txt
C2["Freigabe<br/>Bedarfsplanung"]:::txt
D2["Planungs-<br/>beschluss"]:::txt
E2["Realisierungs-<br/>beschluss"]:::txt
F2["Freigabe<br/>Leistungsverzeichnisse"]:::txt
G2["Vergabe"]:::txt
H2[" "]:::ghost
I2["Abnahme /<br/>Übergabe"]:::txt
J2[" "]:::ghost
end
style row2 fill:transparent,stroke:transparent
A2 --- B2 --- C2 --- D2 --- E2 --- F2 --- G2 --- H2 --- I2 --- J2

%% Projektziele / PPH
subgraph row3[" "]
direction LR
P0["Projektidee"]:::bar
P1["PPH 1"]:::bar
P2["PPH 2"]:::bar
P3["PPH 3"]:::bar
P4["PPH 4"]:::bar
P5["PPH 5"]:::bar
end
style row3 fill:transparent,stroke:transparent
P0 --- P1 --- P2 --- P3 --- P4 --- P5

%% Leistungsphasen
subgraph row4[" "]
direction LR
L0["Leistungs-<br/>phasen"]:::txt
L1["1"]:::bar
L2["2"]:::bar
L3["3"]:::bar
L4["4"]:::bar
L5["5"]:::bar
L6["6 + 7"]:::bar
L8["8"]:::bar
L9["9"]:::bar
end
style row4 fill:transparent,stroke:transparent
L0 --- L1 --- L2 --- L3 --- L4 --- L5 --- L6 --- L8 --- L9

%% Management-Ebenen
subgraph row5[" "]
direction LR
M1["Entscheidungsmanagement"]:::soft
M2["Änderungsmanagement"]:::soft
end
style row5 fill:transparent,stroke:transparent
M1 --- M2

subgraph row6[" "]
direction LR
W0[" "]:::ghost
W1["Wirtschaftlichkeits-<br/>untersuchungen"]:::soft
W2[" "]:::ghost
end
style row6 fill:transparent,stroke:transparent
W0 --- W1 --- W2

%% Untere Arbeitspakete
subgraph row7[" "]
direction LR
Z1["Auftrag<br/>Projektentwicklung"]:::txt
Z2["Kosten-<br/>schätzung"]:::txt
Z3["Kostenberechnung<br/>Baubeschluss"]:::txt
Z4["bearb. Gewerke"]:::bar
Z5["LV + Vergabe"]:::bar
Z6["Abnahme / Übergabe"]:::bar
end
style row7 fill:transparent,stroke:transparent
Z1 --- Z2 --- Z3 --- Z4 --- Z5 --- Z6

subgraph row8[" "]
direction LR
X0[" "]:::ghost
X1["Planung"]:::bar
X2["Nachbearbeitung"]:::soft
X3[" "]:::ghost
end
style row8 fill:transparent,stroke:transparent
X0 --- X1 --- X2 --- X3

%% Unsichtbare Ausrichtung
A -.-> A2
B -.-> B2
C -.-> C2
D -.-> D2
E -.-> E2
F -.-> F2
G -.-> G2
H -.-> H2
I -.-> I2
J -.-> J2

A2 -.-> P0
B2 -.-> P1
D2 -.-> P2
F2 -.-> P3
H2 -.-> P4
I2 -.-> P5

C -.-> L0
D -.-> L1
D -.-> L2
D -.-> L3
E -.-> L4
F -.-> L5
G -.-> L6
H -.-> L8
I -.-> L9

P1 -.-> M1
P3 -.-> M2
P2 -.-> W1

B -.-> Z1
D -.-> Z2
E -.-> Z3
F -.-> Z4
G -.-> Z5
I -.-> Z6
D -.-> X1
I -.-> X2
```

## Hinweis
GitHub erzwingt je nach Oberfläche oft einen dunklen Mermaid-Hintergrund.  
Darum sind jetzt **alle Texte und Balken in weißen Boxen mit schwarzer Schrift** gesetzt, damit nichts mehr „verschwindet“.
