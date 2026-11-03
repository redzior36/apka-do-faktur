# Apka do Faktur — strona aplikacji

Publiczna witryna informacyjna, polityka prywatności, warunki korzystania i kontakt. Repozytorium zawiera wyłącznie stronę; kod aplikacji AdF pozostaje prywatny.

## Adresy docelowe

- Strona główna: https://adf.rdztech.pl/
- Prywatność: https://adf.rdztech.pl/privacy.html
- Warunki: https://adf.rdztech.pl/terms.html
- Kontakt: https://adf.rdztech.pl/contact.html
- Logo do ekranu zgody: https://adf.rdztech.pl/assets/oauth-logo-120.png

Autor: redzior36. Kontakt publiczny: redzior36@gmail.com.

## GitHub Pages i DNS

GitHub Pages publikuje katalog główny gałęzi main. Plik CNAME wskazuje adf.rdztech.pl. Strony nie wymagają JavaScript, logowania, zewnętrznych fontów ani systemu budowania i nie dodają analityki.

W strefie rdztech.pl w Cloudflare:

| Typ | Nazwa | Cel | Proxy |
|---|---|---|---|
| CNAME | adf | redzior36.github.io | Tylko DNS (szara chmurka) |

Cel rekordu nie zawiera https:// ani nazwy repozytorium. Nie zmieniaj rekordów strony głównej domeny, poczty ani konfiguracji repozytorium altstore-source.

Przy uruchamianiu domeny najpierw ustaw ją w Pages tego repozytorium, następnie dodaj rekord DNS. Po wykryciu DNS GitHub wystawia certyfikat; sprawdź jego gotowość i włącz Enforce HTTPS. Nie zgłaszaj do Google adresu z niedziałającym HTTPS.

## Google OAuth

Nazwa aplikacji: Apka do Faktur. E-mail kontaktowy: redzior36@gmail.com. Użyj logo PNG 120 × 120 z assets/oauth-logo-120.png; łączy ikonę aplikacji z pełną nazwą.

Weryfikacja własności: w Google Search Console dodaj usługę typu Domena dla rdztech.pl, używając konta będącego właścicielem projektu Google Cloud. Dodaj w Cloudflare osobny rekord TXT dla @ z dokładną wartością google-site-verification otrzymaną od Google i zatwierdź weryfikację. Zachowaj istniejące rekordy TXT, w tym SPF. Nie zastępuj tej procedury weryfikacją samego prefiksu URL.

W Google Auth Platform → Branding ustaw:

| Pole | Wartość |
|---|---|
| Nazwa | Apka do Faktur |
| Autoryzowana domena | rdztech.pl |
| Strona główna | https://adf.rdztech.pl/ |
| Polityka prywatności | https://adf.rdztech.pl/privacy.html |
| Warunki korzystania | https://adf.rdztech.pl/terms.html |

Podłączenie strony nie zmienia identyfikatorów klientów OAuth ani adresów powrotu aplikacji Apple. Zgodnie z komunikatem otrzymanym od Google po potwierdzeniu własności odczekaj 24 godziny przed ponowną próbą weryfikacji. Dopiero pozytywna ocena Google potwierdza zatwierdzenie marki.

Materiały marki odpowiadają ikonie wersji 0.9.2 aplikacji. Instrukcje: [GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site), [Google — weryfikacja domeny](https://support.google.com/cloud/answer/13804266?hl=en).
