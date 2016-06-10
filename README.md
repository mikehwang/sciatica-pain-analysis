# Sciatica Pain Analysis

This project entails an analysis of a *pain* log that was kept for about 3 weeks from 2016-05-23 to 2016-06-10.  The purpose of the log plus analysis is to help determine if the pain is getting worse and to help assist in the decision making of getting surgery.  The intent is not to identify *"fixes"* for the pain nor to identify causes of the pain rather just track the pain.

## What was logged?

The existence of pain was logged and decomposed into pain types (e.g. aching, sharp, tingling) and pain areas (e.g. calf, buttock, back).

Pain levels were not captured because of its challenge in accurately and consistently sampling this information.  However, the answers to `should surgery` and to `is hopeful` can be an indirect way to gauge pain level.  In moments of great pain, `should surgery` and `is hopeful` are 1 and 0 respectively.

### Fields

Note that the type called boolean was represented as a numerical 0 (false, no, absent) or 1 (true, yes, exists) in the dataset.

Name | Type | Description
--- | --- | ---
record date | date | date of sample
record time | time | local time of sample
record datetime | datetime | datetime of sample
ankle: ache	| boolean | aching in the ankle
calf: ache	| boolean | aching in the calf
calf: sharp	| boolean | sharp pain in the calf
calf: tight	| boolean | muscles feel tight in the calf
calf: tingling	| boolean | pins-and-needles, tingling sensation in the calf
leg: numb	| boolean | parts of the leg feel numb
thigh: ache	| boolean | aching in the back of the thigh
buttock: ache	| boolean | aching in the buttock
back: numb	| boolean | numb feeling in the lower back 
back: sore	| boolean | soreness/aching in the lower back
back: stiff	| boolean | lower back and midsection are stiff, lack of pain-free motion
should surgery	| boolean | "Should I opt for the surgical procedure right at this moment?"
is hopeful	| boolean | "Am I hopeful that I can recover without the surgical procedure?"
posture	| string | position and posture of the body 
is good posture	| boolean | "Do I have good posture meaning is my spine in a good form?"
activity	| string | "What am I doing now?"
activity prev	| string | "What did I do previously?"
notable | string | arbitrary notes to things thought important

## How were entries logged?

A best effort was taken to log entries consistently: consistently in frequency and consistently in unbias collection.  The records were kept in a Google Sheet because:

1. The file could be accessed easily from many devies which lowers the challenge in data collection
2. The hotkey `Ctrl - :` (prints current date) and `Ctrl - Shift - :` (prints current local time) are crucial in recording time easier and consistent

Some columns were added in the middle of the data collection period because new sensations were observed.  The previous records were marked as zero when columns are added rather than a blank or a `NA`. 
