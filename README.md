This file was generated on 20170730 by Simon Podhajsky

-------------------
GENERAL INFORMATION
-------------------

1. Title of Dataset: **Preliminary plans of SIPS 2017 attendeees**
2. Author Information
    * Principal Investigator Contact Information
          * Name: **David Condon**
              * Institution: Northwestern University
              * Email: david-condon@northwestern.edu
    * Associate or Co-investigator Contact Information
          * Name: **Simon Podhajsky**
              * Institution: Yale University
              * Email: simon.podhajsky@yale.edu
3. Date of data collection (single date, range, approximate date) **20170713-20170725**
4. Geographic location of data collection (where was data collected?): **online**
5. Information about funding sources that supported the collection of the data: **COS / its funders**


--------------------------
SHARING/ACCESS INFORMATION
-------------------------- 

1. Licenses/restrictions placed on the data: **MIT**
2. Links to publications that cite or use the data: -
3. Links to other publicly accessible locations of the data: -
4. Links/relationships to ancillary data sets: -
5. Was data derived from another source? -
6. Recommended citation for the data: **_forthcoming_**

---------------------
DATA & FILE OVERVIEW
---------------------

1. File List
    A. Filename: **`people.csv`** 
        * Short description: Properties of SIPS attendees
    B. Filename: **`event_plans.csv`**     
        * Short description: Plans for events by participant, with description of events
2. Relationship between files: **`people.csv` provides participant data for `event_plans.csv` (one-to-many)**
3. Additional related data collected that was not included in the current data package: **~~flexible plans,~~ participant registration**
4. Are there multiple versions of the dataset? ~~yes/~~**no**

--------------------------
METHODOLOGICAL INFORMATION
--------------------------

1. Description of methods used for collection/generation of data (include references): **Google Form sent to registered participants via e-mail**
2. Methods for processing the data: **Export to CSV, then run `tidying_sips_plans.Rmd`**
3. Instrument- or software-specific information needed to interpret the data: **none, but R 3.4+ preferred**
4. Standards and calibration information, if appropriate: **-**
5. Environmental/experimental conditions: **-**
6. Describe any quality-assurance procedures performed on the data: **-**
7. People involved with sample collection, processing, analysis and/or submission: **Katie & Brian & others in the SIPS 2017 org team (collection), Simon (processing & analysis), David (submission)**

## Data-specific information

### `event_plans.csv`

1. Number of variables: **5**
2. Number of cases/rows: **1260**
3. Variable List
     A. Name: **`participant_ID`**
          * Description: **unique participant index linked to the person data in `people.csv`**
     B. Name: **`event_type`**
          * Description: **The format of the event the participant is planning to attend**
          * Possible values: **Social, Hack, Re-hack, Workshop, Flexible, `NA`** _(and meanings)_
     C. Name: **`event_time`**
          * Description: **The start and, if applicable, end of the event**
          * Possible values: **No standard format ("12p-1a")**
     D. Name: **`event_day`**
          * Description: **The day on which the event takes place, relative to the conference start**
          * Possible values: **0-3**
4. Missing data codes:
     * `NA`: **No checkbox selected for a given day / data cannot be provided for the given event**
5. Specialized formats of other abbreviations used: **-**

### `people.csv`
1. Number of variables: **5**
2. Number of cases/rows: **166**
3. Variable List
     A. Name: **`participant_ID`**
          * Description: **unique participant index**
          * Possible values: **non-repeating integers**
     B. Name: **`time_submitted`**
          * Description: **The timestamp in ET timezone at which the submission was received by Google servers**
     C. Name: **`email_server`**
          * Description: **The part of the email address after the '@' sign**
     D. Name: **`number_names`**
          * Description: **The number of space-separated names that the participant listed**
          * Possible values: 1-4
4. Missing data codes: **-**
5. Specialized formats of other abbreviations used: **-**