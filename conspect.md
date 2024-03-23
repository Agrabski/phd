Platformy no-code oferują, osobom bez wykształcenia technicznego, możliwość tworzenia aplikacji.
W zastosowaniach przemysłowych, pozwalają one na wytwarzanie oprogramowania przez ekspertów domenowych, bez angażowania profesjonalnych programistów.
Logikę programów no-code tworzy się z gotowych komponentów, tzw. Aktywności, odpowiadających instrukcjom z typowych jęzków programowania.
Poza prostymi operacjami, takimi jak przypisanie zmiennej, instrukcje warunkowe czy pętle, zwykle dostępne są też bardziej zaawansowane, specyficzne dla procesów biznesowych, bloki.
Typowym przykładem jest wysyłanie wiadomości email, pobieranie danych z systemów zewnętrzynch oraz zarządzanie użytkownikami w systemach takich jak Active Directory.

Platformy no-code ułatwiają proces wytwarzania oprogramowania, ale nie zastępują całkowicie kompetencji programistycznych.
Tworzenie aplikacji w ten sposób, można zrozumieć jako programowanie w języku bardzo wysokiego poziomu.
W związku z tym, aplikacje no-code są podatne na występowanie tych samych klas defektów i mogą skorzystać na dostępie do tych samych narzędzi i technik, co programy w klasycznych językach programowania.

Celem tej pracy jest zaadaptowanie narzędzi oraz technik występujących w tradycyjnej inżynierii oprogramowania, do programowania no-code, w sposób przystępny dla osób bez wykształcenia technicznego.
Proponowane rozwiązania będą powstawać w ramach platformy CasePro 8, następcy szeroko używanego w Polskiej bankowości CasePro 7.
W szczególności badane będą następujące obszary:
- Analiza statyczna zamodelowanej logiki i zapewnianie poprawności modelu. 
Podstawowym pytaniem badawczym będzie w tym aspekcie sprawdzenie, w jakim stopniu aplikacje no-code wymagają tworzenia dedykowanych narzędzi do weryfikacji.
W tym celu zbadana zostanie możliwość użycia analizatorów języka C# na modelu no-code przez generowanie ekwiwalentnego, ale niekompletnego, kodu C# na podstawie modelu procesu.
- Automatyzacja testów powstałych aplikacji.
- Przyśpieszanie tworzenia aplikacji, przez generowanie fragmentów modelu.
Zbadane zostanie zarówno zastosowanie prostych algorytmów herustycznych, pracujących na ręcznie przygotowanych szablonach jak i adaptacji Generatywnej Sztucznej Inteligencji (GSI).
Istotnym wyzwaniem do pokonania, przy wykorzystaniu GSI będzie brak dostępnych danych treningowych, specyficznych dla systemu CP8.
- Przyśpieszanie nauki wytwarzania aplikacji no-code.
Badanym zagadnieniem będzie wykorzystanie sztucznej inteligencji do wyjaśniania działania procesu bądź aktywności, w połączeniu z ręcznie przygotowaną biblioteką przykładowych modeli.

Najważniejszym aspektem tej pracy jest zapewnienie przystępności stworzonych narzędzi dla osób bez wykształcenia technicznego.
W tym celu, na obecnych użytkownikach platformy CasePro zostaną przeprowadzone badania sprawdzające zrozumienie diagnostyk, powszechność stosowania testów automatycznych oraz użyteczność automatycznie generowanego modelu.
Ponadto, konsturkcja języka w którym model aplikacji jest wyrażany, zostanie przeanalizowany pod kątem elementów promujących wytwarzanie poprawnych rozwiązań, bądź ich utrudniających.