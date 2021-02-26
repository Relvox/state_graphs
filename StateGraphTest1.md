# Graph 1 - Basic Meep

## Data

+ `stats : health:int * mana:int * water:int * food:int`

* `max, current, rates : stats`
* `vision_radius, scan_interval : int`
* `age : int`
* `memory_magnitude : int`
* `awake.`
  * `resting threshold : int`
* `resting.`
  * `time_to_wake : int`

### Defaults

## States

* `awake`
* `thinking`
* `resting : initial`
* `dead`

## Transitions

* ```   
  [current.health <= 0] 
  -> dead
  ```
* ```
  resting ->
  tick
  [time_to_wake == 0]
  -> awake
  ```
* ```
  resting ->
  tick
  [time_to_wake > 0]
  {time_to_wake = time_to_wake - 1}
  ```