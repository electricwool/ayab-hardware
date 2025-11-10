# AYAB Hardware

Check the release page for the files. https://github.com/electricwool/ayab-hardware/releases/tag/ayab

This is the KiCAD converted to EasyEDA Pro format with real world practical considerations for PCB manufacture and current BOM.
solder pads left in place but parts are not selected for impractical and commonplace connectors such as 2.54mm headers that are of no use to anyone and parts that require cutting the case apart that nobody wants to do. tiny smd buttons are placed instead for firmware programming purposes.

Japanese caps. SMD not through hole because small through hole from quality brands are niche, expensive and arn't typically stocked by fabs.
preference for "basic" parts that do not incur additional loading charges. Fabs keep the machines loaded with parts and charge additional fees per part when they need to manually load parts in to the parts placement machine. 
basic red LEDs were out of stock so they have been replaced with blue LEDs and absurd resistor values like 10k series resistors changed accordingly for 5mA LEDs.

when ordering your board select ENIG to avoid production failures.

Why?

It is free design software that permits rapid export to JLCPCB by persons with no knowledge of electronics for the production of fully assembled boards including PCBA. total cost is about USD$50 per board including shipping when ordering 5 or more at a time and economy shipping that is about the same price as a DIY AYAB arduino shield kit being sold on etsy and elsewhere.

known bug: silkscreen has too many layers and is too complex to import so silkscreen layers appear solid white and can't be editted in EasyEDA. important parts have been simply labelled in plain text.

only parts not available at the fab are power connectors and hirose connectors. These can be soldered yourself easily.

power connectors:

These so-called "Custom" headers allegedly artisinally whittled by Brother engineers according to AYAB docs are actually JST V-series connectors.
cut down to 5-pin and 4-pin.

2x RTB-1.5-6P,JST https://www.aliexpress.com/item/1005008477785335.html

kh910 hirose connectors:

1x HNC2-2.5P-3DS02 https://mou.sr/3JtELXj

1x HNC2-2.5P-8DS55 https://mou.sr/49bmMPH

2x HNC2-2.5P-10DS55 https://mou.sr/4oxmlUA

additionally if you wish to get rid of the dangerous old japanese appliance plug and 40 year old cable that came with the machine you may convert the machine to 12V by using a plug of your choice and 3D printing this plate. https://www.thingiverse.com/thing:7002037 it provides a convenient way to connect 12V to the ayab board unlike the current design that has the barrel jack needing to obstruct the needle bed.
