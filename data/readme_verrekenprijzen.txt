Source: http://www.tennet.org/bedrijfsvoering/ExporteerData.aspx

info can be found on: http://www.tennet.org/bedrijfsvoering/Systeemgegevens_afhandeling/verrekenprijzen/index.aspx

------------------------------------------------------------------------------

decimal separetor is comma. This is manually replaced

------------------------------------------------------------------------------

Headers raw file
[datum]
[PTE]
[periode_van]
[periode_tm]
[noodvermogen]:Noodvermogen, indien vermeld, is een indicator voor de inzet noodvermogen; dit beïnvloedt de vaststelling van de onbalansprijs.
[opregelen]: Opregelen, indien vermeld, geldt de verrekenprijs van gebruikte biedingen aan opregelzijde: TenneT betaalt de bieder deze prijs.
[Afregelen]: Afregelen, indien vermeld, geldt de verrekenprijs van gebruikte biedingen aan afregelzijde: de bieder betaalt TenneT TSO deze prijs (bij een negatieve prijs betaalt TenneT de bieder).
[prikkelcomponent]: "De prikkelcomponent is onderdeel van de onbalansprijs en is bedoeld ter stimulering van het daadwerkelijk nakomen door marktpartijen van door TenneT gebruikte biedingen regel- en reservevermogen voor balanshandhaving en balansherstel en als prikkel om de te verrekenen onbalans te minimaliseren"
see also:
http://www.tennet.org/bedrijfsvoering/Systeemgegevens_afhandeling/prikkelcomponent/Prikkelcomponent.aspx
[Afnemen]: Afnemen wordt altijd vermeld en geldt de verrekenprijs van onbalans van de PV's met tekort: de PV betaalt TenneT TSO deze prijs (indien negatief betaalt TenneT de PV).
[invoeden]: Invoeden wordt altijd vermeld en geldt de verrekenprijs van onbalans van PV's met overschot: TenneT betaalt de PV deze prijs (indien negatief betaalt de PV TenneT)
[regeltoestand]: De Regeltoestand wordt altijd vermeld en heeft de waarde –1, 0, 1 of 2 en is van invloed op de vaststelling van de onbalansprijs. 

--------------------------------------------------------------------------------

Headers clean file
datetime: local datetime

noodvermogen: if noodvermogen is called 1 otherwise zero

opregelen: price for ramping up powerplant

Afregelen: price for rmaping down powerplant

prikkelcomponent:
http://www.tennet.org/bedrijfsvoering/Systeemgegevens_afhandeling/prikkelcomponent/prikkelcomponent_2006.aspx
De prikkelcomponent is onderdeel van de onbalansprijs en is bedoeld ter stimulering van het daadwerkelijk nakomen door marktpartijen van door TenneT gebruikte biedingen regel- en reservevermogen voor balanshandhaving en balansherstel en als prikkel om de te verrekenen onbalans te minimaliseren.

Afnemen: price for being short. Extracting from the grid

invoeden: price for being long. Feeding to the grid

regeltoestand:


