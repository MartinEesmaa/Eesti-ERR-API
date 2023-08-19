# Eesti rahvusringhääling API dokumentatsioon

Tere tulemast Eesti rahvusringhääling API dokumentatsioon abi.

[Eesti rahvusringhääling](err.ee) API dokumentatsioon abi on programmeerijatele ja vaatajatele võivad uurida informatsiooni, kuidas ERR süsteem veebist töötab.

Alusta veebiaadressiga, et võtta API informatsioon veebist:

www.err.ee/api/[AADRESS SIIA]

Tegevus | Aadress | Kirjeldus | Küsimus märk / Lisu saadaval | Saadaval käsk
--- | --- | --- | --- | --- |
POST | statistics/articleStatistics | Saadab kliendi interneti brauser informatsiooni ERR-isse | Ei
GET | electricityMarketData/get | Võta elektri börsihind andmed tänaselt ja homselt | Ei
GET | geoblock/inEstonia | Kontrolli külastaja elab Eestis või mitte. | Ei
GET | radioSchedule/getExactSchedules | Loe täpselt ajakava raadiod kanalis. | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn)
GET | tvSchedule/getExactSchedules | Loe täpselt ajakava televiisorid kanalis. | Jah (vajalik) | `channel` (etv, etv2, etvpluss)
GET | language/getLanguageJson | Võta keel kõik tekstilt JSON-is. | Jah (vajalik) | `categoryId` (109 - Eesti, 110 - Vene, 130 - Inglise)
GET | feeds/GetTVFeed | Loeb portaal informatsioon, näitab ERR uudised äpp ainult öösel kõik ERR kanalid. | Jah (vajalik) | `portal` (uudised, kultuur, sport, menu, teadus, rus)
GET | live/getChannelByName | | Jah (vajalik)
GET | tv/getCategoryPastShows | | Jah (vajalik)
GET | tvSchedule/getTimelineSchedule | Loeb ajaskaala ajakava televiisoril | Jah (vajalik) | `channel` (etv, etv2, etvpluss), `day` (mis päev?), `month` (mis kuu?) ja `year` (mis aasta?).
GET | radioSchedule/getTimelineSchedule | Loeb ajaskaala ajakava televiisoril | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn), `day` (mis päev?), `month` (mis kuu?) ja `year` (mis aasta?).
GET | geoblock/getRegionalData | Kontrolli külastaja elab Eestis või Euroopa Liidus, muud mitte. | Ei
GET | tv/getTvPageData | | Jah (vajalik)
GET | currentViewers/getChannelViewers | Võta arvu vaatajad kanalist internetis | Jah (vajalik) | `channel` (etv, etv2, etvpluss, vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn)
GET | content/getHtml/ | Loeb HTML väike koodi ükskõik artikli numbrit uudiselt. | Jah (vajalik)
GET | photo/getById | Loe foto ID. | Jah (vajalik)
GET | content/getNextFor/ | Võta teine artikel pärast esimest. | Jah (vajalik)
GET | poll/get/ | | Ei
GET | tvSchedule/getTimelineSchedule2 | Loeb ajaskaala ajakava televisoori, annab rohkem informatsioone | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn), `day` (mis päev?), `month` (mis kuu?), `year` (mis aasta?), `portal` (milline portaal?).
GET | radioSchedule/getTimelineSchedule2 | Loeb ajaskaala ajakava raadiol, annab rohkem informatsioone | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn), `day` (mis päev?), `month` (mis kuu?), `year` (mis aasta?), `portal` (milline portaal?).
GET | rds/getForChannel | | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn)
GET | category/latest | | Jah (vajalik)
GET | radio/getRadioPageData | | Jah (vajalik)
GET | search/getContents | Otsib tekstid ERR otsingumootoriga. | Jah (vajalik)
GET | time/getTimestamp | Võta aeg numbrit | Ei
GET | captcha/get | Võta CAPTCHA juhuslik | Jah (vajalik) | `lang` (et, en, rus)
POST | content/addLike/ | Pandakse meeldiva nuppu järel saatmine serverisse. | Jah (vajalik) | Vaja artiklit number uudises
OPTIONS | publicUser/checkAuthentication | Kontrollib, et kas kasutaja on logitud sisse või mitte ja küpsised olemas | Ei
GET | category/last24h | Võta viimased 24 tundi informatsiooni | Jah (vajalik)
GET | mobile/getErrAppMenu | Võta kõik ERR äppi menüüst linkid. | Ei
GET | mobile/getNewsAppMenu | Võta ERR Uudised ainult äppi menüüst linkid. | Ei
GET | radio/getProgramSeriesData | | Jah (vajalik) | `channel` (vikerraadio, raadio2, klassikaraadio, raadio4, raadiotallinn)
GET | v2/menu/getMenuById | Loeb ERR ülemenüü või kategooriad avalehes | Jah (vajalik) | `menuId` (555 - Eesti, 781 - Vene, 1049 - Üle menüü)
GET | v2/vodContent/getContentPageData | | Jah (vajalik)
GET | v2/category/getByUrl | Loeb külastatud linki näha kategooriad | Jah (vajalik)
GET | v1/menu/777 | Loeb ERR ülemenüü kategooriad avalehes |
GET | v1/frontpage | Loeb ERR arhiiv esileht
GET | v1/profile
POST | auth/login | Logida sisse koos e-post aadress ja salasõna | Jah (vajalik) | `user` ja `pass`
POST | publicUser/validateData | Registreerida konto koos e-post aadress ja salasõna | Jah (vajalik) | `email` ja `pass`

- Martin Eesmaa