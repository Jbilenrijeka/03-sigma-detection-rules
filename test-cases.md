# Manual test cases

| Case | Event | Expected result | Why |
|---|---|---|---|
| 1 | EventID 4625 | Match first rule | Failed logon event |
| 2 | EventID 4624 | No match first rule | Successful logon |
| 3 | PowerShell process with `-EncodedCommand` | Match second rule if field mapping matches | Encoded command keyword |
| 4 | Approved admin script with encoded command | May match; investigate context | Possible false positive |

The first rule detects a failed-logon event, not a brute-force sequence by itself. Repeated-event correlation needs a SIEM correlation rule or an appropriate aggregation feature.
