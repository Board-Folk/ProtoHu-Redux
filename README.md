# ProtoHu Redux

## A Simple flash HuCard for the NEC PC Engine/Turbo-Grafx range of consoles.

This project is based upon David Shadoff's [ProtoHu](https://github.com/dshadoff/ProtoHu_revA).
The original Eagle project was converted to KiCad. The most important
difference is the addition of an OR gate to fully decode the HuCard
address space, such that the image written to the flash is available
only in the lower half and not mirrored the the upper one. The
motivation for this is for the card to respond to the minimum practical
range of addresses in the HuCard space, freeing the upper region such
that diagnostic tests may be performed without risk of conflicts with
hardware in a real console. Specifically, this card can be flashed with
diagnostics for the CD hardware found in a PC Engine/Turb Duo system.


## PCB Production

The project consists of two boards: one that features the HuCard
connector and all the components, the other being a spacer to fit under
the first to give the complete assembly a flat lower surface. The upper
board should be 0.8mm thick with at least an ENIG finish for gold
plating on the edge connector contacts. A chamfered edge near the
connector will improve the fit.

The spacer board should be 1.6mm to clear the height of the components and
bring the total up to 2.4mm, which seems to be the nominal dimension of a
standard HuCard. As it contains no components, the finish on the spacer
boards is not important.

This visual design is intended to look vaguely like an original HuCard
when white solder mask is used with black silkscreen.


## Assembly

Suggested order of operations:

* Populate IC1, IC2, then the passives and finally the header pins.
* Dry fit the two boards to test.
* When satisfied, use CA/super glue or similar to join the two boards. Some
  areas labeled "GLUE" are left unmasked to ensure direct adhesion to the
  board substrate, but glue can also be applied anywhere else you deem fit.
