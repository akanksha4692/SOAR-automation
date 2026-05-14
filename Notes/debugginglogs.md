Issue 1 : Missing artifacts
### Problem
collect2() returned empty data.

### Root Cause
Artifacts were not properly added to the event.

### Fix
Disabled artifact dependency and recreated artifacts correctly.

Issue 2 : Nonetype error
### Error
TypeError: int() argument must be a string, a bytes-like object or a real number, not 'NoneType'

### Root Cause
baseEventCount field existed but contained null value.

### Fix
Added validation before type conversion.

Issue 3 — Runtime Data Type Mismatch
### Error
save_run_data(): value must be an unencoded string

### Root Cause
save_run_data only accepts string values.

### Fix
Converted integer to string before storing runtime data.
