 [![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
 
 # Swiss Parliamentary Speeches
The dataset contains all speeches given in the [Swiss Parliament](https://www.parlament.ch) since the 1999 winter session (*Wintersession 1999*) as well as further information on the speakers, the items of business discussed and the debate. The data were collected using web scraping and are updated at irregular intervals. 

## Download Link
https://www.gfzb.ch/swisspoliticalspeeches/20190910.rds

## Codebook
| Variable | Description |
| --- | --- |
| `s_transcript_raw` | Raw transcript of the speech as extracted from the website of the [Swiss Parliament](https://www.parlament.ch). |
| `s_transcript` | Speech without unspoken content (brackets, page references) |
| `s_speaker_name` | Name  of the speaker |
| `s_speaker_council` | Council of the speaker *(BR = Bundesrat (Federal Council), BK = Bundeskanzler (Federal Chancellor), NR = Nationalrat (National Council), SR = Ständerat (Council of states))* |
| `s_speaker_canton` | Canton of the speaker ([2-letter abbreviation](https://en.wikipedia.org/wiki/Data_codes_for_Switzerland#Cantons), only for NR and SR) |
| `s_speaker_faction` | [Faction affiliation](https://www.parlament.ch/en/organe/groups) of the speaker |
| `s_speaker_president` | Dummy variable, if `s_speaker_president == 1` the speaker is council president (subsequently coded by date) |
| `s_link` | Link to the original transcript on the website of the [Swiss Parliament](https://www.parlament.ch) |
| `s_link_video` | Link to video of the speech on the website of the [Swiss Parliament](https://www.parlament.ch) |
| `s_language_cld2` | Main language detected by [cld2](https://github.com/CLD2Owners/cld2) (subsequently coded) |
| `s_length_words` | Length of the non-raw transcript in words (subsequently coded) |
| `b_number` | ID of the discussed item of business |
| `b_title_german` | Title of the discussed item of business in german |
| `b_title_french` | Title of the discussed item of business in french |
| `b_link` | Link to the item of business on the website of the [Swiss Parliament](https://www.parlament.ch) |
| `d_session` | Session of the debate |
| `d_date` | Date of the debate *(YYYY-MM-DD)* |
| `d_time` | Start time of the debate (HHhMM) |
| `d_council` | Council of debate *(NR = Nationalrat (National Council), SR = Ständerat (Council of states), VB = Vereinigte Bundesversammlung (United federal Assembly))* |
| `d_preliminary` | Dummy variable, if `d_preliminary == 1` the transcripts of the debate are preliminary. |
| `scraping_timestamp` | Time of scraping |

## Proposed Citation
Zumbach, David (2019). *Swiss Parliamentary Speeches (1999-2019)*. Zürich: Grünenfelder Zumbach GmbH.

## Publications and applications
* [Anthology on "Konkordanz" in the Swiss Parliament (Bühlmann et al. 2019)](https://www.nzz-libro.ch/konkordanz-im-parlament-zwischen-kooperation-und-konkurrenz-politik-und-gesellschaft-in-der-schweiz)
* [Blog post on defacto.expert on the federal diversity in Switzerland (Mueller/Zumbach 2017)](https://www.defacto.expert/2017/12/21/foederale-vielfalt-im-schweizer-parlament/)
