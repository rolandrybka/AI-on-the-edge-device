# Parameter `HoldLastValidValue`
Default Value: `true`

If enabled, a reading rejected by the maximum-rate check, the negative-rate check, or because it contains an unreadable digit returns the last valid meter value instead of an empty value. The rejected reading is not saved as the new previous value. Once a later reading is accepted, the returned value advances normally.

This does not correct an incorrectly recognized value that is within the configured maximum rate. Configure `<NUMBER>.MaxRateValue` to a realistic upper bound for the consumption between readings.

Only used if a valid previous value is available.

!!! Note
    If you edit the config file manually, prefix this parameter with `<NUMBER>` followed by a dot (e.g. `main.HoldLastValidValue`). The reason is that this parameter is specific for each `<NUMBER>` (`<NUMBER>` is the name of the number sequence defined in the ROI's).
