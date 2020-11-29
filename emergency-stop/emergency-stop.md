# Overview

The woody and possibly metalkworking area need some form or emergency stop
system to quickly remove power when an emergency condition is signalled by
a user.

The design goals are:

- The system should initialise in an safe (off) state.
- The system should be quick to shut off power on emergency signal
- The system should be resilent to damage to parts

Either we will have to design our own control or find a pre-existing
solution which we can buy.


## Ben's design for a system

The directory has a design based on trying to meet the above requirements
in an simple way, without resorting to complicated control systems. This
is to try and produce something that can be easily built, serviced and
reasoned about.

Each room will have the following:

- one or more emergency stop buttons
- one central box for circuitry
- one control panel with the following controls
  - stop
  - reset
  - lockout

The control box is the only point where the system can be reset to
on. If one of the stop points is still engaged then the reset switch
will not work. The lockout switch will also override the reset and
keep the system off until disengaged (and then the system will require
the reset switch to put the power back on)


The central box contains the contactor to control the power and a
small circuit to action the rest of the controls.

Still to be decided:

- will reset require holding for a minimum time to allow reset?
- should the control circuitry be run off low-voltage 12/24V ?


## Emergency stop buttons

The choices here are cheap-ish from ebay for around £6 per button or
look at some of the choices from high-class suppliers. The cheapest
so far is Rapid where if we want to get 10 they are about £11-ex-vat
per button.

Currently not sure if there is a recommendation, but my initial idea
is that someone should not be more than 2M away from an emergency
stop. This would mean probably 3 per long wall, and one on each of the
middle pillars. total = 8 for woody.


https://www.ebay.co.uk/itm/Red-Sign-Mushroom-Emergency-Stop-Push-Button-Switch-Station-1-No-1-Nc-GF-od/353213267022

https://uk.farnell.com/camdenboss/csc1-50/switch-e-stop-40mm-red-release/dp/2083457

https://www.rapidonline.com/hylec-1de-01-01ag-ip66-e-stop-button-twist-release-station-78-2107

https://www.cef.co.uk/catalogue/products/406931-1-way-plastic-emergency-stop-twist-release-pushbutton-station

## Contactor

The main disconnect for the power. It is difficult to work out what an
appropriate contact would be. The minium woudl be to be able to disconnect
expect loads (mainly motors) which requires AC3 rating.

It might be we need to down-rate the circuits to 16A to make use of cheaper
contactors. Currnently the circuits are both on C20 RCBOs in the board behind
woody.

Questions to still be answered:

- Can we isolate just the "live" or do we need to disconnect both L&N?

Notes/References:

- https://www.se.com/uk/en/faqs/FA136111/
- https://www.se.com/us/en/faqs/FA120833/

# Rough costs for woody

£20 for the control box (already have suitable enclosure)
£20 for the electronics
£60-£250 for the contactor
£6-£15 x 8 for switches (£48 - £120)

total £148 to £410 for woody, probably similar for metalworking.
Note, for metalworking a new enclosure would be required)

The big issue for this is chosing the right contactor



