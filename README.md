# Electricity Price Forecasting in the Central European Region Using Machine Learning Algorithms


This is my [thesis work](https://diplomaterv.vik.bme.hu/hu/Theses/Villamosenergiaar-elorejelzese-a-kozep) of the master's degree. The dataset I use in my thesis work is from the [ENTOSE Transparancy Platform](https://transparency.entsoe.eu/content/static_content/Static%20content/web%20api/Guide.html). In order to get the data I use the [ENTSOE-PY API](https://github.com/EnergieID/entsoe-py).


Any re-use or publication of any part of the content is only allowed with the written consent of the author.

2024 (c) Botond Bendegúz Prohászka<br/>
Consulent and supervisor: Csaba Gáspár

---
Budapest University of Technology and Economics <br>
Faculty of Electrical Engineering and Informatics <br>
Department of Telecommunications and Media Informatics



# Notes

Ma 8as adatokkal 9ig a holnapit (a mait mind ismerem)
- baseline1 az 1 heti adat
- baseline2 hasonló időjárású nap

Kiértékelés:
- v1 abs hiba (hány eurót tévedtünk)
- v2 adott órában mennyi a load (termelés / fogyasztás), hiba súlyozva a teljes fogyasztással

Opciók
- recurrent nn predictor (?)
- gbm regressor
-- (előzö napi adatok, napelemek termelése, román adatok, hőmérséklet..., körny ország árai)
-- walk forward opt

keretrendszer
feture inportance alapján feature selection 
- változásuk követése !!!

(talán osztrák is számít, meg kell nézni melyik számít)

időjárási adatok (első körben tényadatok, nem előrejelzés) próbálkozni kell, drága lehet, kb kizárt 

- végén fontos és ***nem fontos*** változók listája

3 fontos időjárás (régiós, a napi bontás is jó)
- hány fok van (fűtés / hűtés)
- besugárzás
- szélerősség


-Hányszor volt negatív ár - statisztika róla (Meg tudjuk-e mondani, hogy mikor lesz negatív ár)
-- Ez is lehet célváltozó és kiértékelés

- Napi egy órát kikapcsoljuk, cél: mikor legyen (mert a többi órában többet tudunk termelni)
-- Meg lehet nézni, hogy melyik lesz a legdrágább óra

