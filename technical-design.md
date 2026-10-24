# Technical Design Document --- GlucoWAVE

## 1. Project goal

Investigate the RF response of a microstrip patch antenna and an
FSS-related structure as early-stage engineering work toward a proposed
non-invasive glucose-monitoring concept. An AMC configuration and a
direct FSS-versus-AMC comparison are planned but have not yet been
completed.

## 2. Design concept

The antenna is modelled in CST Studio Suite. Changes in the
electromagnetic properties of the surrounding environment can affect
antenna response. Candidate parameters for analysis include resonant
frequency, S-parameter magnitude and phase, input impedance, bandwidth,
and efficiency.

These parameters are not uniquely indicative of glucose concentration.
Tissue composition, hydration, temperature, placement, geometry, and
other factors may affect the response. The present simulation work
should therefore be treated as antenna research rather than a validated
glucose measurement method.

## 3. Architecture and simulation workflow

``` mermaid
flowchart TD
    A[Define antenna geometry and materials] --> B[Build patch model in CST]
    B --> C[Configure feed, boundaries, mesh and frequency sweep]
    C --> D[Run electromagnetic simulation]
    D --> E[Review S-parameters and far-field output]
    E --> F[Record configuration and result metrics]
    F --> G[Review current patch and FSS-related results]
    G --> H[Future work: develop AMC configuration]
    H --> I[Future work: compare FSS and AMC under equivalent conditions]
```

## 4. Current implementation status

  -----------------------------------------------------------------------
  Work item                           Status
  ----------------------------------- -----------------------------------
  Microstrip patch antenna design     Completed in CST

  Patch antenna S-parameter           Result plot available
  simulation                          

  Patch far-field simulation          Result plot available;
                                      configuration association needs
                                      confirmation

  FSS-related structure               CST model and response plot
                                      available

  AMC design and simulation           Not yet completed

  FSS-versus-AMC comparison           Pending AMC simulation

  Physical fabrication / VNA testing  Not reported as completed

  Glucose-reference dataset /         Not currently available
  calibrated model                    
  -----------------------------------------------------------------------

## 5. Current simulation results

Values summarized from the available CST result plots are listed in
[`../results/simulation-results.md`](../results/simulation-results.md)
and
[`../results/current-simulation-results.csv`](../results/current-simulation-results.csv).
Supporting plot images are provided in `../results/figures/`.

## 6. Evaluation plan

For each configuration, record the same applicable metrics: - Resonant
frequency (GHz) - Relevant S-parameter magnitude and phase, with
port/result definition - Input impedance (Ω) - Bandwidth using a stated
criterion - Radiation and total efficiency, when available - Directivity
/ radiation pattern, when relevant

A fair comparison requires consistent frequency ranges, tissue/model
conditions, solver settings, and clearly documented differences between
configurations.

## 7. Reproducibility and data handling

Each reported value should be traceable to a CST project version, run
identifier, model configuration, frequency sweep, port definition, and
exported result. When direct numerical exports become available, use
them as the primary data source and retain plots as supporting evidence.

## 8. Next steps

1.  Export numerical S-parameter data and simulation settings from CST.
2.  Confirm the FSS-related result curve definition and the model
    associated with far-field results.
3.  Complete the AMC configuration.
4.  Compare FSS and AMC using the same evaluation metrics and equivalent
    simulation conditions.
5.  If glucose-related sensing is pursued, establish controlled
    tissue-model variations and validate against reference measurements.

## 9. Scope and safety

GlucoWAVE is an engineering research concept, not a medical device. The
current results do not establish glucose-monitoring accuracy or HbA1c
estimation. Clinical use would require substantial further development,
calibration, and independent validation.
