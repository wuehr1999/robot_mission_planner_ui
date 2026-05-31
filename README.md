# robot_mission_planner

## Specifications

- An interactive map is the core of the UI
- Wayoint coordinates can be loaded into the application via a form
- Waypoint coordinates can be selected by clicking on the map
- Options can be defined for every waypoint (e. g. drop balls for RoboOrienteering)
- A route can be configured by selecting the waypoints on the map
- Different speeds can be selected for every route segment
- The route can be exported as JSON to transfer it to the robots control software:
~~~bash
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Generated schema for Root",
  "type": "object",
  "properties": {
    "route": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "latitude": {
            "type": "number"
          },
          "longitude": {
            "type": "number"
          },
          "speed": {
            "type": "number"
          },
          "options": {
            "type": "string"
          }
        },
        "required": [
          "latitude",
          "longitude",
          "speed",
          "options"
        ]
      }
    }
  },
  "required": [
    "route"
  ]
}
~~~