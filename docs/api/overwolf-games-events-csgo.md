---
id:overwolf-games-events-csgo
title: CS:GO Game Events
sidebar_label: CS:GO Events
---

Please read the [overwolf.games.events](overwolf-games-events) documentation page to learn how to use Overwolf game events.

:::important Game ID
7764
:::

## Sample Apps

* [CS:GO game events sample app](https://github.com/overwolf/events-sample-apps)

## Available Features

* [match_info](#match_info)
* [kill](#kill)
* [death](#death)
* [assist](#assist)
* [headshot](#headshot)
* [round_start](#round_start)
* [match_start](#match_start)
* [match_info](#match_info)
* [match_end](#match_end)
* [team_round_win](#team_round_win)
* [bomb_planted](#bomb_planted)
* [bomb_change](#bomb_change)
* [reloading](#reloading)
* [fired](#fired)
* [weapon_change](#weapon_change)
* [weapon_acquired](#weapon_acquired)
* [info](#info)
* [roster](#roster)
* [player_activity_change](#player_activity_change)
* [team_set](#team_set)
* [replay](#replay)
* [counters](#counters)

## `kill`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
kill        | totalKills – total kills for player in match |Player has killed an enemy| | 0.70  |

## `death`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
death        | totalDeaths – total deaths of player in match |Player has died| | 0.70  |

## `assist`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
assist        | 	totalAssists – total assists for user it match |Player has assisted in killing an enemy| | 0.70  |

## `headshot`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
headshot    | headshotsInRound – total headshots for user in <b>current round</b> |Player has gained a killed with a headshot| Fired alongside kill event	 | 0.70  |

## `round_start`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
round_start | <ul><li>num_of_rounds – total number of rounds in current match</li><li>player_team – CT/T</li> | A new round has began | |     0.70      |

## `match_start`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
match_start |     None     |A new match has started|            |      0.70     |

## `match_end`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
match_end   |     None     |Match was ended|                    |      0.70     |

## `team_round_win`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
team_round_win|     None     |<ul><li>winningTeam – the team that won the round (CT/T)</li><li>bomb – bomb status (exploded/defused/planted)|   |      0.70     |
  
## `bomb_planted`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
bomb_planted|     None     |A bomb has been planted (by any player)|            |      0.70     |

## `bomb_change`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
bomb_change |Bomb state (planted / exploded / defused)|Bomb state was changed|  |      0.70     |

## `reloading`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
reloading |<ul><li>weapon_name</li><li>weapon_current_ammo</li><li>weapon_max_ammo</li><li>weapon_type| Player reloads his weapon | |0.70
  
## `fired`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
fired       |<ul><li>weapon_name</li><li>weapon_current_ammo</li><li>weapon_max_ammo</li><li>weapon_type|  | "fired" is not available on "Arms Race" and "Demolition" modes | 0.70  |
  
## `weapon_change`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
weapon_change| <ul><li>weapon_name</li><li>weapon_type |Player switches weapons| See [notes](#weapon_change-note) | 0.70  |

#### *weapon_change* note

* **weapon_type:**

```json
"Knife", "Pistol", "Shotgun", "Machine Gun", "Submachine Gun", "Rifle", "SniperRifle", "Grenade", "C4"
```

* **weapon_name:**

```json
"weapon_knife", "weapon_knife_t", "weapon_hkp2000", "weapon_usp_silencer", "weapon_glock", "weapon_elite",  "weapon_p250", "weapon_fiveseven", "weapon_cz75a","weapon_tec9", "weapon_deagle", "weapon_revolver", "weapon_nova", "weapon_xm1014", "weapon_mag7","weapon_sawedoff", "weapon_m249", "weapon_negev",  "weapon_mp9", "weapon_mac10", "weapon_mp7",  "weapon_ump45", "weapon_p90", "weapon_bizon","weapon_famas", "weapon_galilar", "weapon_m4a1",  "weapon_m4a1_silencer", "weapon_ak47","weapon_ssg08", "weapon_aug", "weapon_sg556", "weapon_awp", "weapon_scar20", "weapon_g3sg1","weapon_incgrenade", "weapon_decoy", "weapon_flashbang", "weapon_hegrenade", "weapon_smokegrenade", "weapon_c4"
```

## `weapon_acquired`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
weapon_acquired| <ul><li>weapon_name</li><li>weapon_type |Player acquires new weapon (either buy or picks up)|  | 0.70  |

## `player_activity_change`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
player_activity_change | <ul><li>playing</li><li>menu |<ul><li>The player started playing</li><li>The player entered the game’s menu | | 0.70  |

## `team_set`

### Events

Event       | Event Data   | Fired When    | Notes              | Since Version |
------------| -------------| --------------| ------------------ | --------------|
team_set    |<ul><li>CT</li><li>T|The player selected a team|   |      0.70     |


## `match_info`

### Info Updates

key               | Category    | Values                    | Notes                 | Since Version |
----------------- | ------------| ------------------------- | --------------------- | ------------- |
pseudo_match_id | match_info  |	The current session’s ID code. See [notes](#pseudo_match_id-note)	| | 0.130  |
server_info | match_info  |	The current session’s server ID. See [notes](#server_info-note)	| | 0.135  |

#### *pseudo_match_id* note

This is an Overwolf-generated code, unrelated to Steam.

Data Example:

```json
0c0ea3df-97ea-4d3a-b1f6-f8e34042251f
```

#### *server_info* note

Data Example:

```json
{"match_info":{"server_info":"{"name":"RU | ALTAI AWP [!ws,!knife,!gloves,!viptest] 128tick","ip":"212.22.93.74:27040"}"}}
```

## `info`

### Info Updates

key               | Category    | Values                    | Notes                 | Since Version |
----------------- | ------------| ------------------------- | --------------------- | ------------- |
totalKills | player  |	Total kills in a match	            |                       |    0.70       |
totalDeaths | player  |	Total deaths in a match		    |                       |    0.70       |
totalMvps | player  |	Total MVP’s	 	            |                       |     0.70       |
score | player  |	Score in a match	            |                       |     0.70       |
team | player  |	T / CT	                            |                       |     0.70       |
steamid | player  |	The player’s steam id	            |                       |     0.70       |
map | round            |	Map name	            |                       |     0.70       |
mode | round  |	Map mode (for example: "casual")            |                       |     0.70       |
numOfRound | round  |	Round number in the match (starting 0)|                     |     0.70       |
phase | round  |Match phase<ul><li>warmup</li><li>live</li><li>freezetime</li><li>over|    |     0.70       |
scene | scene  |<ul><li>MainMenu</li><li>LoadingScreen</li><li>Game</li><li>MenuInGame(ESC)|  |     0.70       |

## `roster`

### Info Updates

key               | Category    | Values                    | Notes                 | Since Version |
----------------- | ------------| ------------------------- | --------------------- | ------------- |
lobby | roster  |JSON containing array of lobby_players objects. See [notes](#lobby-note)|  |     0.77       |
match | roster  |JSON containing array of player objects. See [notes](#match-note)|  |     0.77       |

#### *lobby* note

Each player contains:

* steamId

Data Example:

```json
{
    "feature":"roster",
    "category":"roster",
    "key":"lobby",
    "value":"{"lobby_players\" : [{"steamId\":"76561198269560618"}]}"}
```

#### *match* note

Each player contains:

* steamId
* team

Data Example:

```json
{
    "feature":"roster",
    "category":"roster",
    "key":"match",
    "value":"{"players" : [
            {"steamId":"76561198364007097","team":"Counter-Terrorists"},{"steamId":"76561198389957131","team": "Counter-Terrorists"}
    ]}"}
```

## `replay`

### Info Updates

key               | Category    | Values                    | Notes                 | Since Version |
----------------- | ------------| ------------------------- | --------------------- | ------------- |
replay_list       | replay      | See [notes](#replay-note) |                       |     134.0     |

#### *replay* note

Values:

A list containing the URL address of all available replays that are currently stored in your profile (can be accessed via the main menu under "Your Matches").

Data Example:

`{"category":"game_info","key":"replays_list","value":"{"replays":[{"link": "steam://rungame/730/76561202255233023/+csgo_download_match%20CSGO-dVoC5-kwY8k-LCb3J-wCiMw-CrahQ","order":"0"},{"link": "steam://rungame/730/76561202255233023/+csgo_download_match%20CSGO-myDzD-AOTzm-wYZzH-bCmrA-JebRF","order":"1"}]}","valueLength":261}
16:06:54.359 InfoDBContainer.js:69 [InfoDBContainer] UPDATING INFO (decoded): {"feature":"replay","category":"replay","key":"replay_list","value":"["steam://rungame/730/76561202255233023/+csgo_download_match CSGO-dVoC5-kwY8k-LCb3J-wCiMw-CrahQ","steam://rungame/730/76561202255233023/+csgo_download_match CSGO-myDzD-AOTzm-wYZzH-bCmrA-JebRF"]"}`

## `counters`

### Info Updates

key               | Category    | Values                    | Notes                 | Since Version |
----------------- | ------------| ------------------------- | --------------------- | ------------- |
ping              | performance | Latency to server         |                       |               |
