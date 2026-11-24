# Dataset README

This repository contains the CSV files used in the study of repeated news exposure, article ordering strategies, and participants’ political views. The files contain participant survey responses, article metadata and text, article interactions, and reading events.

## Files and how they relate

| File | Contents | Typical unit of observation |
|---|---|---|
| [`userdata.csv`](userdata.csv) | Participant and Prolific demographics, study assignment, and session timing. | One row per participant. |
| [`stancedata.csv`](stancedata.csv) | Topic, ordering strategy, and stance, Overton Window, and advocate-evaluation measures from up to four surveys. | One row per participant. |
| [`interactiondata.csv`](interactiondata.csv) | Article IDs grouped by whether they were viewed, liked, disliked, or assigned each agreement response. | One row per participant. |
| [`articlesreadingdata.csv`](articlesreadingdata.csv) | Recorded article viewing events and their start/end times and duration. | One row per article-view event. |
| [`articlesdata.csv`](articlesdata.csv) | Article text and metadata, including topic, position strength, stance, model, and platform IDs. | One row per article record. |
| [`masterdata.csv`](masterdata.csv) | A combined participant-level file containing participant details, stance measures, and interaction fields. | One row per participant. |

`masterdata.csv` combines fields also present in `userdata.csv`, `stancedata.csv`, and `interactiondata.csv`; these files are overlapping views of the data, not independent samples. Participant files can generally be linked by `uniqueID`; `prolificID` is the participant’s Prolific identifier. Article and interaction records can be linked using the article/post IDs. Keep the distinction between `postId`, `viewPostId`, `articleCsvId`, and `articleIdBCKP`: they are identifiers from different data exports and should not be assumed interchangeable without checking the relevant records.

## Column descriptions

### `userdata.csv`

| Column | Description |
|---|---|
| `prolificID` | Participant identifier from Prolific. |
| `uniqueID` | Study/platform participant identifier; used to link study files. |
| `age` | Value in the `age` field. Supplied rows look like birth years rather than ages; verify before treating this as age. |
| `gender` | Participant’s reported gender. |
| `education` | Participant’s reported highest education category. |
| `employment` | Participant’s reported employment category. |
| `hasVoted` | Response to the study’s voting-history question. |
| `politicalActivities` | Response to the study’s political-activity question. |
| `politicalMember` | Response about political-party or political-organization membership. |
| `newsFrequency` | Reported frequency of following/reading news (first recorded field). |
| `newsFrequency2` | Second news-frequency response as stored in the export. |
| `newsSource` | Reported news sources; multiple selections may appear in one cell. |
| `Status` | Prolific submission status. |
| `Total approvals` | Prolific approval count as supplied in the participant export. |
| `race` | Participant’s reported race/ethnicity category. |
| `countryBirth` | Country of birth as reported. |
| `countryNow` | Country of current residence as reported. |
| `Nationality` | Reported nationality. |
| `Language` | Reported language. |
| `S1Time` | Recorded duration/time value for study session 1. |
| `batch` | Recruitment or data-collection batch label. |
| `S2Time` | Recorded duration/time value for study session 2. |
| `S3Time` | Recorded duration/time value for study session 3. |

### `stancedata.csv`

| Column | Description |
|---|---|
| `prolificID` | Participant identifier from Prolific. |
| `uniqueID` | Study/platform participant identifier. |
| `topic` | Selected political topic: abortion, military armament, or social media regulation. |
| `rankstrat` | Assigned article-ordering condition (`control`, `center`, or `edge`). |
| `SQ1stance` | Ideological stance measure at survey 1; see the study measures/code for its transformation and scale. |
| `SQ1OWmin` | Lower endpoint of the participant’s estimated Overton Window at survey 1. |
| `SQ1OWmax` | Upper endpoint of the participant’s estimated Overton Window at survey 1. |
| `SQ1feelterm` | Ideological thermometer/self-placement response at survey 1. |
| `SQ1oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 1. |
| `SQ1oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 1. |
| `SQ1oneMoral` | Evaluation of side one advocates on the morality item, survey 1. |
| `SQ1oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 1. |
| `SQ1oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 1. |
| `SQ1oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 1. |
| `SQ1twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 1. |
| `SQ1twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 1. |
| `SQ1twoMoral` | Evaluation of side two advocates on the morality item, survey 1. |
| `SQ1twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 1. |
| `SQ1twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 1. |
| `SQ1twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 1. |
| `SQ2stance` | Ideological stance measure at survey 2; see the study measures/code for its transformation and scale. |
| `SQ2OWmin` | Lower endpoint of the participant’s estimated Overton Window at survey 2. |
| `SQ2OWmax` | Upper endpoint of the participant’s estimated Overton Window at survey 2. |
| `SQ2feelterm` | Ideological thermometer/self-placement response at survey 2. |
| `SQ2oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 2. |
| `SQ2oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 2. |
| `SQ2oneMoral` | Evaluation of side one advocates on the morality item, survey 2. |
| `SQ2oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 2. |
| `SQ2oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 2. |
| `SQ2oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 2. |
| `SQ2twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 2. |
| `SQ2twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 2. |
| `SQ2twoMoral` | Evaluation of side two advocates on the morality item, survey 2. |
| `SQ2twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 2. |
| `SQ2twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 2. |
| `SQ2twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 2. |
| `SQ3stance` | Ideological stance measure at survey 3; see the study measures/code for its transformation and scale. |
| `SQ3OWmin` | Lower endpoint of the participant’s estimated Overton Window at survey 3. |
| `SQ3OWmax` | Upper endpoint of the participant’s estimated Overton Window at survey 3. |
| `SQ3feelterm` | Ideological thermometer/self-placement response at survey 3. |
| `SQ3oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 3. |
| `SQ3oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 3. |
| `SQ3oneMoral` | Evaluation of side one advocates on the morality item, survey 3. |
| `SQ3oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 3. |
| `SQ3oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 3. |
| `SQ3oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 3. |
| `SQ3twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 3. |
| `SQ3twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 3. |
| `SQ3twoMoral` | Evaluation of side two advocates on the morality item, survey 3. |
| `SQ3twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 3. |
| `SQ3twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 3. |
| `SQ3twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 3. |
| `SQ4stance` | Ideological stance measure at survey 4; see the study measures/code for its transformation and scale. |
| `SQ4OWmin` | Lower endpoint of the participant’s estimated Overton Window at survey 4. |
| `SQ4OWmax` | Upper endpoint of the participant’s estimated Overton Window at survey 4. |
| `SQ4feelterm` | Ideological thermometer/self-placement response at survey 4. |
| `SQ4oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 4. |
| `SQ4oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 4. |
| `SQ4oneMoral` | Evaluation of side one advocates on the morality item, survey 4. |
| `SQ4oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 4. |
| `SQ4oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 4. |
| `SQ4oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 4. |
| `SQ4twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 4. |
| `SQ4twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 4. |
| `SQ4twoMoral` | Evaluation of side two advocates on the morality item, survey 4. |
| `SQ4twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 4. |
| `SQ4twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 4. |
| `SQ4twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 4. |


The `one` and `two` prefixes refer to the two topic sides as presented in the study. The side-to-position mapping depends on topic: side 1 is pro-choice for abortion, pro-armament for military armament, and pro-regulation for social media regulation; side 2 is the opposing position. The exact response anchors and derived-score formulas should be taken from the study questionnaire and analysis code.

### `interactiondata.csv`

Each interaction cell contains a serialized list of article/post IDs. An empty list (`[]`) means no IDs were recorded for that response category in that row.

| Column | Description |
|---|---|
| `uniqueID` | Study/platform participant identifier. |
| `liked` | IDs of articles the participant liked. |
| `disliked` | IDs of articles the participant disliked. |
| `viewed` | IDs of articles recorded as viewed. |
| `agreement_1` | IDs of articles assigned agreement response 1. |
| `agreement_2` | IDs of articles assigned agreement response 2. |
| `agreement_3` | IDs of articles assigned agreement response 3. |
| `agreement_4` | IDs of articles assigned agreement response 4. |
| `agreement_5` | IDs of articles assigned agreement response 5. |
| `agreement_6` | IDs of articles assigned agreement response 6. |
| `agreement_7` | IDs of articles assigned agreement response 7. |
| `agreement_8` | IDs of articles assigned agreement response 8. |
| `agreement_9` | IDs of articles assigned agreement response 9. |
| `agreement_10` | IDs of articles assigned agreement response 10. |


### `articlesreadingdata.csv`

| Column | Description |
|---|---|
| `userId` | Platform user identifier associated with the reading event. |
| `username` | Platform username associated with the event. |
| `username_second` | Second username field in the source export; its distinct purpose is not documented in the CSV. |
| `uniqueID` | Study/platform participant identifier, when available. |
| `prolificID` | Prolific participant identifier, when available. |
| `viewPostId` | Identifier for the recorded post-view event. |
| `postId` | Platform post/article identifier. |
| `startTime` | Timestamp when the article-view event began. |
| `endTime` | Timestamp when the article-view event ended. |
| `DurationSeconds` | Duration value stored for the event. In the supplied rows, values such as `18,819` match milliseconds (18.819 seconds) when compared with the start/end timestamps, despite the column name. Verify units and decimal/thousands parsing before analysis. |
| `session` | Session label, when present; some rows may be blank. |

### `articlesdata.csv`

| Column | Description |
|---|---|
| `articleCsvId` | Article identifier/index used in the CSV export. |
| `title` | Article headline/title. |
| `body` | Article text, including HTML markup where present. |
| `topic` | Political topic assigned to the article. |
| `strength` | Intended position-strength level of the article. |
| `stance` | Political position advocated by the article. |
| `postId` | Platform post identifier associated with the article. |
| `articleIdBCKP` | Backup/source article identifier retained in the export. |
| `postTitle` | Title stored for the corresponding platform post. |
| `postTopic` | Topic stored for the corresponding platform post. |
| `postStrength` | Position-strength value stored for the corresponding platform post. |
| `postStance` | Stance stored for the corresponding platform post. |
| `postCreatedAt` | Timestamp when the platform post was created. |
| `postUpdatedAt` | Timestamp when the platform post was last updated. |
| `model` | Language model recorded as the article’s source/generator. |

### `masterdata.csv`

`masterdata.csv` contains the columns from the participant, stance, and interaction exports in one participant-level table. Its fields have the same meanings as the matching columns described above. For completeness, every field is listed here.

| Column | Description |
|---|---|
| `prolificID` | Participant identifier from Prolific. |
| `uniqueID` | Study/platform participant identifier. |
| `age` | Value in the `age` field. Supplied rows look like birth years rather than ages; verify before treating this as age. |
| `gender` | Participant’s reported gender. |
| `education` | Reported highest education category. |
| `employment` | Reported employment category. |
| `hasVoted` | Response to the voting-history question. |
| `politicalActivities` | Response to the political-activity question. |
| `politicalMember` | Response about party/organization membership. |
| `newsFrequency` | First recorded news-frequency response. |
| `newsFrequency2` | Second news-frequency response as stored in the export. |
| `newsSource` | Reported news sources; multiple selections may appear in one cell. |
| `Status` | Prolific submission status. |
| `Total approvals` | Prolific approval count as supplied in the export. |
| `race` | Reported race/ethnicity category. |
| `countryBirth` | Country of birth as reported. |
| `countryNow` | Country of current residence as reported. |
| `Nationality` | Reported nationality. |
| `Language` | Reported language. |
| `S1Time` | Recorded duration/time value for session 1. |
| `batch` | Recruitment or data-collection batch label. |
| `S2Time` | Recorded duration/time value for session 2. |
| `S3Time` | Recorded duration/time value for session 3. |
| `topic` | Selected political topic. |
| `rankstrat` | Assigned ordering condition (`control`, `center`, or `edge`). |
| `SQ1stance` | Ideological stance measure at survey 1; see study code for its transformation and scale. |
| `SQ1OWmin` | Lower endpoint of the estimated Overton Window at survey 1. |
| `SQ1OWmax` | Upper endpoint of the estimated Overton Window at survey 1. |
| `SQ1feelterm` | Ideological thermometer/self-placement response at survey 1. |
| `SQ1oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 1. |
| `SQ1oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 1. |
| `SQ1oneMoral` | Evaluation of side one advocates on the morality item, survey 1. |
| `SQ1oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 1. |
| `SQ1oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 1. |
| `SQ1oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 1. |
| `SQ1twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 1. |
| `SQ1twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 1. |
| `SQ1twoMoral` | Evaluation of side two advocates on the morality item, survey 1. |
| `SQ1twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 1. |
| `SQ1twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 1. |
| `SQ1twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 1. |
| `SQ2stance` | Ideological stance measure at survey 2; see study code for its transformation and scale. |
| `SQ2OWmin` | Lower endpoint of the estimated Overton Window at survey 2. |
| `SQ2OWmax` | Upper endpoint of the estimated Overton Window at survey 2. |
| `SQ2feelterm` | Ideological thermometer/self-placement response at survey 2. |
| `SQ2oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 2. |
| `SQ2oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 2. |
| `SQ2oneMoral` | Evaluation of side one advocates on the morality item, survey 2. |
| `SQ2oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 2. |
| `SQ2oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 2. |
| `SQ2oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 2. |
| `SQ2twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 2. |
| `SQ2twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 2. |
| `SQ2twoMoral` | Evaluation of side two advocates on the morality item, survey 2. |
| `SQ2twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 2. |
| `SQ2twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 2. |
| `SQ2twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 2. |
| `SQ3stance` | Ideological stance measure at survey 3; see study code for its transformation and scale. |
| `SQ3OWmin` | Lower endpoint of the estimated Overton Window at survey 3. |
| `SQ3OWmax` | Upper endpoint of the estimated Overton Window at survey 3. |
| `SQ3feelterm` | Ideological thermometer/self-placement response at survey 3. |
| `SQ3oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 3. |
| `SQ3oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 3. |
| `SQ3oneMoral` | Evaluation of side one advocates on the morality item, survey 3. |
| `SQ3oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 3. |
| `SQ3oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 3. |
| `SQ3oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 3. |
| `SQ3twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 3. |
| `SQ3twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 3. |
| `SQ3twoMoral` | Evaluation of side two advocates on the morality item, survey 3. |
| `SQ3twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 3. |
| `SQ3twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 3. |
| `SQ3twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 3. |
| `SQ4stance` | Ideological stance measure at survey 4; see study code for its transformation and scale. |
| `SQ4OWmin` | Lower endpoint of the estimated Overton Window at survey 4. |
| `SQ4OWmax` | Upper endpoint of the estimated Overton Window at survey 4. |
| `SQ4feelterm` | Ideological thermometer/self-placement response at survey 4. |
| `SQ4oneOpenmind` | Evaluation of side one advocates on the open-mindedness item, survey 4. |
| `SQ4oneModerate` | Evaluation of side one advocates on the moderation/extremity item, survey 4. |
| `SQ4oneMoral` | Evaluation of side one advocates on the morality item, survey 4. |
| `SQ4oneFamily` | Social-distance response about having a side one advocate as a immediate-family member, survey 4. |
| `SQ4oneFriend` | Social-distance response about having a side one advocate as a close friend, survey 4. |
| `SQ4oneCoworker` | Social-distance response about having a side one advocate as a coworker, survey 4. |
| `SQ4twoOpenmind` | Evaluation of side two advocates on the open-mindedness item, survey 4. |
| `SQ4twoModerate` | Evaluation of side two advocates on the moderation/extremity item, survey 4. |
| `SQ4twoMoral` | Evaluation of side two advocates on the morality item, survey 4. |
| `SQ4twoFamily` | Social-distance response about having a side two advocate as a immediate-family member, survey 4. |
| `SQ4twoFriend` | Social-distance response about having a side two advocate as a close friend, survey 4. |
| `SQ4twoCoworker` | Social-distance response about having a side two advocate as a coworker, survey 4. |
| `liked` | IDs of liked articles (serialized list). |
| `disliked` | IDs of disliked articles (serialized list). |
| `viewed` | IDs of viewed articles (serialized list). |
| `agreement_1` | IDs of articles assigned agreement response 1 (serialized list). |
| `agreement_2` | IDs of articles assigned agreement response 2 (serialized list). |
| `agreement_3` | IDs of articles assigned agreement response 3 (serialized list). |
| `agreement_4` | IDs of articles assigned agreement response 4 (serialized list). |
| `agreement_5` | IDs of articles assigned agreement response 5 (serialized list). |
| `agreement_6` | IDs of articles assigned agreement response 6 (serialized list). |
| `agreement_7` | IDs of articles assigned agreement response 7 (serialized list). |
| `agreement_8` | IDs of articles assigned agreement response 8 (serialized list). |
| `agreement_9` | IDs of articles assigned agreement response 9 (serialized list). |
| `agreement_10` | IDs of articles assigned agreement response 10 (serialized list). |
