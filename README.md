# hue-morse

# copied from here: https://www.youtube.com/watch?v=Wz8GnB-LI5w

###Get device state 

**Definition**

`GET service.controller.hue/device/<device-identifier>`

**Response**

— `200 OK` on success

— `404 NOT FOUND` if the device does not exist 

```json

{
  "identifier":  "bedroom-lamp",
  "name": "Bedroom Lamp",
  "type": "huelight",
  "state": {
    "brightness": {
      "type": "int",
      "min": 0,
      "max": 100,
      "value": 73
    },
    "power": {
      "type": "bool",
      "value": true
      }
   }
}
```

### Update a device

**Definition**

`PATCH service.controller.hue/device/<device-identifier>`

**Arguments**
The properties to change and their new values.

**Response**
— `200 OK` on success
— `404 NOT FOUND` if the device does not exist 
— `400 BAD REQUEST` if request validation fails 
