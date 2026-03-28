# IVR Flow Explanation

## Flow Steps

1. User selects "Pay via Call"
2. System triggers IVR call
3. IVR announces payment details
4. User presses:
   - 1 → Confirm
   - 2 → Cancel
5. System processes request (conceptual)
6. User receives confirmation

## Decision Flow
Start
 ↓
Play Payment Info
 ↓
Wait for Input
 ↓
[1] Confirm → Success
[2] Cancel → Abort
[No Input] → Timeout
