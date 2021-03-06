# Functions

## DefaultFunction

Function name: `default`

if function-name not match any func, use it as default function.

### Params

no param

### Expression

`y = 0`

---

## LinearFunction

Function name: `StandardLinearFunction`

### Params

- slope
- offsetX
- offsetY

### Expression

Input: x (`int64`)

`y = slope * (x + offsetX) + offsetY`

### Inner set:

`DefaultLinearFunction`

- slope: 1
- offsetX: 0
- offsetY: 0

`ReverseLinearFunction`

- slope: -1
- offsetX: 0
- offsetY: 0

---

## RandomFunction

Function name `StandardRandomFunction`

### Params:

- range
- seed
- base-point

### Expression

rand generate by seed

y = base-point + rand()

base-point <= y <= base-point + range(ceil)

## LinearPeak function

Function name `StandardLinearPeak`

### Params:

- range
- offsetX
- offsetY
- ratio

### Expression

`y = ratio * ((x + offsetX) % range) + offsetY`

### Inner set:

`SecondLinearPeak`

- range: 1
- ratio: 1
- offsetX: 0
- offsetY: 0

`MinuteLinearPeak`

- range: 60
- ratio: 1
- offsetX: 0
- offsetY: 0

`HourLinearPeak`
- range: 3600
- ratio: 1
- offsetX: 0
- offsetY: 0

`DayLinearPeak`
- range: 86400
- ratio: 1
- offsetX: 0
- offsetY: 0