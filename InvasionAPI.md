The Invasion API provides an automatically updated json object with a list of all active invasions, which include the district, the cog invading the district, invasion size, cogs defeated, and timestamps.

### API url: https://www.projectaltis.com/api/invasion

Example returned data:


```json
{
  "lastUpdated": "1488644485",
  "friendlyLastUpdated": "1 second ago",
  "serverPopulation": 61,
  "districts": [
    {
      "Nuttyboro": {
        "population": 14,
        "status": true,
        "lastUpdated": "1488644485",
        "friendlyUpdatedAt": "1 second ago",
        "invasion": {
          "cog": "Bossbot",
          "size": 1,
          "defeated": 1
        }
      }
    },
    {
      "Nutty River": {
        "population": 18,
        "status": true,
        "lastUpdated": "1488644484",
        "friendlyUpdatedAt": "1 second ago",
        "invasion": {
          "cog": "Lawbot",
          "size": 1,
          "defeated": 1
        }
      }
    },
    {
      "Sillyham": {
        "population": 16,
        "status": true,
        "lastUpdated": "1488644448",
        "friendlyUpdatedAt": "37 seconds ago",
        "invasion": false
      }
    },
    {
      "Geezer Gorge": {
        "population": 13,
        "status": true,
        "lastUpdated": "1488644472",
        "friendlyUpdatedAt": "13 seconds ago",
        "invasion": false
      }
    }
  ]
}

```

### Returned data

lastUpdated: last time updatred, in unix/epoch time.
friendlyLastUpdated: friendly name for last updated.
serverPopulation: total TTPA population.

districts: array of district objects:
- district Name
 - population
 - status: online or not?
 - lastUpdated: last updated in unix/epoch time.
 - friendlyUpdatedAt: friendly name for last updated.
 - invasion: false if not an invasion, object if it is:
    - Cog: Cog type (for now)
    - Size: placeholder
    - defated: placeholder
