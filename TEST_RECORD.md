# Test record

Each rule was tested separately with all other fields valid.

| Test | Expected result | Actual result | Pass/Fail |
|---|---|---|---|
| Empty required fields | Blocked with feedback; no success | Error message shown, no success | Pass |
| Email: amina | Blocked | Blocked | Pass |
| Telephone: 123 | Blocked | Blocked | Pass |
| Portfolio blank | Accepted | Success preview | Pass |
| Portfolio: https://example.com | Accepted | Success preview | Pass |
| Portfolio: not-a-url | Blocked | Blocked | Pass |
| Date: yesterday | Blocked | Blocked | Pass |
| Date: today | Accepted | Success preview | Pass |
| Seats: 0 | Blocked | Blocked | Pass |
| Seats: 5 | Blocked | Blocked | Pass |
| Seats: 1.5 | Blocked | Blocked | Pass |
| Seats: 1 | Individual booking | "individual booking for 1 seat" | Pass |
| Seats: 4 | Group booking | "group booking for 4 seats" | Pass |
| Short password | Blocked | Blocked | Pass |
| Mismatched confirmation | Blocked | Blocked | Pass |
| Short/mismatched corrected | Success | Success preview | Pass |
| Agreement unchecked | Blocked | Blocked | Pass |
| All fields valid | Green preview; password not shown | Green preview, no password shown | Pass |
| 390px-wide view | No sideways scrolling | Page width = viewport width (390) | Pass |
| Tab navigation | Visible keyboard focus | Purple focus outline on each control | Pass |
