# State Graphs

Like State Charts but meh.

## FSM-Like Concepts

### State Node

* Has Unique String Id
* Exposes `.enter` and `.exit` events

### Transition HyperEdge

* Sources: Ids (Exited in order)
* Events: Names and args
* Guards: Boolean Condition Expression
* Actions: 
  * Send Messages to Queue
  * Set Data Values
  * Invoke Game Actions?
  * Scripted Logic?
* Targets: Ids (Entered in order)

### Data 

* Bools, Ints, Strings
* Trigger `changing($data)` event on data change attempt
  * also `_in(` for internal changes
  * also `_ex(` for external changes
* Trigger `changed($data)` event on data changed

### Events

* Have Name `snake_case`
* Can use Args `($var1,$bloop)`
  * Args are extracted from message or defaults

