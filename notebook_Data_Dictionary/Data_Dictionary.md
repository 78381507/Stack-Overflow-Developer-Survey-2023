# Data Dictionary (selected fields)

## Identifiers
- `ResponseId` (int): unique response ID

## Demographics
- `Age` (str): age band (e.g., "25-34 years old")
- `Country` (str): respondent country
- `EdLevel` (str): education level

## Work & preferences
- `RemoteWork` (str): Remote / Hybrid / In-person
- `Employment` (str): employment status

## Compensation
- `ConvertedCompYearly` (float): annual compensation (converted to a common currency by source provider)
- `CompTotal` (float/str): total compensation as reported

## Experience & satisfaction
- `YearsCodePro` (str): years of professional coding ("Less than 1 year", numeric, "More than 50 years")
- `JobSat` (float): job satisfaction score (0–10)

## Tech stack (multi-select, semicolon-separated)
- `LanguageHaveWorkedWith`, `LanguageWantToWorkWith`
- `DatabaseHaveWorkedWith`, `DatabaseWantToWorkWith`
- `PlatformHaveWorkedWith`, `PlatformWantToWorkWith`

**Note:** Multi-select columns are parsed into individual items for Top-N counts.
