Scenario: Entering poor input
Given:    A negative number (or other such kind of invalid answer) as input from the user
When:     The user tries to submit the answer as their amount of push-ups
Then:     The system should inform the user that it's an invalid answer and prompt for them to re-enter

Scenario: Entering zero input
Given:    A zero as input from the user
When:     The user tries to submit the answer as their amount of push-ups
Then:     The system should NULL out the value, as the lack of a record provides as much information as a record with a value of 0

Scenario: User queries for data that doesn't exist
Given:    That no data was entered for October
When:     The user looks up their average push-ups per day for October
Then:     Display a blank screen with a message "No push-ups recorded for October"

Scenario: Query for data with holes in it
Given:    Only 10 days in October has push-up data recorded
When:     The user looks up their average push-ups per day for October
Then:     Display two sets of day, one with a "true" average for October, one only accounting for days with data entered