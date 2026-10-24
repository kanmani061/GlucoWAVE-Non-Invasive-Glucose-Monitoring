# CST Simulation Results --- Current Stage

This report summarizes the values visible in the project's current CST
result plots. The figures are included in this folder for context. The
numerical values should ultimately be verified against CST-exported data
and saved model/run settings.

## 1. Patch antenna S-parameter result

-   **Resonant frequency:** 2.3972 GHz
-   **Minimum S11:** -47.323 dB
-   **Feed inset parameter (`InL`):** 7.2 mm is visible in a CST
    parameter screenshot; its association with the exact plotted run
    should be retained in the project record.

A strongly negative S11 value indicates low reflected power at that
frequency in the simulated setup. It does not, by itself, demonstrate
glucose sensing.

## 2. FSS-related structure result

-   **Curve minimum:** -32.089 dB
-   **Frequency at minimum:** 2.3899 GHz
-   **CST curve label:** `SZmin(1),Zmax(1)`

The result should be interpreted according to the model's port and
S-parameter definition. Do not label it as S11, S21, reflection, or
transmission until the CST result-tree definition confirms that
interpretation.

## 3. Far-field result at 2.4 GHz

-   **Radiation efficiency:** -4.373 dB
-   **Total efficiency:** -4.391 dB
-   **Directivity:** 5.733 dBi

These values are recorded as a separate far-field result set. The exact
configuration/run that produced them must be associated with the data
before attributing them to the patch or FSS model.

## 4. AMC status

AMC design and simulation have not yet been completed. Consequently, no
AMC performance values or FSS-versus-AMC conclusion are reported.

## 5. Interpretation

The results describe simulated antenna behaviour. They are not measured
glucose values and do not establish a calibrated relationship between
antenna response and glucose or HbA1c. Future comparison should use
exported numerical results, documented model settings, and equivalent
simulation conditions.
