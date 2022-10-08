# Suspicion Avoidance
This page covers everything related to suspicion avoidance settings in `config.yml` file.

## `random_individual_delay`
**Type: INT**

**Recommended Value: false**

Random delay to be added on top of existing delay.



## `random_rate_limit_delay`
**Type: INT**

**Recommended Value: 0**

Random delay to be added on top of the existing ratelimit delay.

## `random_delay_before_dm`
**Type: INT**

**Recommended Value: 10**

Random delay to be added before starting a DM. Useful to avoid detection.



## `typing`
**Type: BOOLEAN**

**Recommended Value: false**

When enabled, tokens show a "typing..." status before sending a DM.


## `typing_variation`
**Type: INT**

**Recommended Value: 250**

Random delay added in typing.

## `typing_speed`

**Type: INT**

**Recommended Value: 300**

Speed in which the message is typed (Affects the overall time it takes to send the message, shorter messages will be sent quicker).


## `typing_base`

**Type: INT**

**Recommended Value: 100**

Base delay added for typing.

