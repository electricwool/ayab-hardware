# AYAB Hardware
This is the KiCAD converted to EasyEDA Pro format with real world practical considerations for PCB manufacture and current BOM.
solder pads left in place but parts are not selected for impractical and commonplace connectors such as 2.54mm headers that are of no use to anyone and parts that require cutting the case apart that nobody wants to do. tiny smd buttons are placed instead for firmware programming purposes.

Japanese caps
preference for "basic" parts that do not incur additional loading charges. Fabs keep the machines loaded with parts and charge additional fees per part when they need to manually load parts in to the parts placement machine. 

when ordering your board select ENIG to avoid production failures.

Why?

it is free design software that permits rapid export to JLCPCB for the production of fully assembled boards including PCBA.

known bug: silkscreen has too many layers and is too complex to import so silkscreen layers appear solid white and can't be editted in EasyEDA.

only parts not available at the fab are power connectors and hirose connectors. These can be soldered yourself easily.

power connectors:

These so-called "Custom" headers allegedly artisinally whittled by Brother engineers are actually JST V-series connectors.
cut down to 5-pin and 4-pin
2x RTB-1.5-6P,JST https://www.aliexpress.com/item/1005008477785335.html

kh910 hirose connectors:

1x https://www.mouser.com/ProductDetail/Hirose-Connector/HNC2-2.5P-3DS02?qs=gyfFsMMHMKzG6FQKazr3xQ%3D%3D
1x https://www.mouser.com/ProductDetail/Hirose-Connector/HNC2-2.5P-8DS55?qs=gyfFsMMHMKyPvUaAz%25252BHWBw%253D%253D
2x https://www.mouser.com/ProductDetail/Hirose-Connector/HNC2-2.5P-10DS55?qs=gyfFsMMHMKwBSYDtzLhaIA%253D%253D
