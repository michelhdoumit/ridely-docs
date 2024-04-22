# Ridely

## Objetivo

O objetivo do projeto Ridely é fortalecer a capacidade de analise e tomada de decisão baseada em contextos. 

```mermind
classDiagram
  class Ride {
    <<entity>>
    status: enum
  }

  class Address {
    <<entity>>
    text: string
    location: geography::point
  }

  class Driver {
    <<entity>>
    name: string
    available: bool
  }

  class Car {
    <<entity>>
    license_plate: string
    model: string
    color: string
  }

  class Passenger {
    <<entity>>
    name: string
  }

  Address "1" -- "1" Ride : pickup
  Address "1" -- "1" Ride : dropoff
  Ride "*" -- "1" Driver : drives
  Ride "*" -- "1" Passenger : rides
  Driver "1" -- "1" Car : owns

```
