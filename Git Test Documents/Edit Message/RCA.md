# Root Cause Analysis (RCA) – Edit Message Bug

## 1. Summary
Edit allowed beyond 15-minute limit.

## 2. Root Cause
Backend missed validation of message timestamp on edit request.

## 3. Impact
Policy violation and potential misuse of feature.

## 4. Fix
Added backend time validation logic and updated API unit tests.

## 5. Preventive Actions
- Add backend validation tests  
- Include boundary time test cases in QA  
- Add logging for late edit attempts
