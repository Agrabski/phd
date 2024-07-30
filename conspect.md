# Generatywna sztuczna inteligencja, analiza statyczna i zarządzanie zależnościami: Inżynieria oprogramowania dla aplikacji low-code

Platformy no-code oferują, osobom bez wykształcenia technicznego, możliwość tworzenia aplikacji.
W zastosowaniach przemysłowych, pozwalają one na wytwarzanie oprogramowania przez ekspertów domenowych, bez angażowania profesjonalnych programistów.
Logikę programów no-code tworzy się z gotowych komponentów, tzw. Aktywności, odpowiadających instrukcjom z typowych jęzków programowania.
Poza prostymi operacjami, takimi jak przypisanie zmiennej, instrukcje warunkowe czy pętle, zwykle dostępne są też bardziej zaawansowane, specyficzne dla procesów biznesowych, bloki.
Typowym przykładem jest wysyłanie wiadomości email, pobieranie danych z systemów zewnętrzynch oraz zarządzanie użytkownikami w systemach takich jak Active Directory.

Platformy no-code ułatwiają proces wytwarzania oprogramowania, ale nie zastępują całkowicie kompetencji programistycznych.
Tworzenie aplikacji w ten sposób, można zrozumieć jako programowanie w języku bardzo wysokiego poziomu.
W związku z tym, aplikacje no-code są podatne na występowanie tych samych klas defektów i mogą skorzystać na dostępie do tych samych narzędzi i technik, co programy w klasycznych językach programowania.

## Przegląd literatury

Temat wytwarzania platform no-code jest obecnie w literaturze poruszany tylko w niewielkim stopniu.
W szczególności wstępny przegląd nie wykazał żadnych artykułów na temat integracji sztucznej inteligencji w proces wytwarzania rozwiązań no-code, ani na temat analizy staycznej tych modeli.
Artykuł Low-Code Platform autorstwa Alexander C. Bock i Ulrich Frank (https://doi.org/10.1007/s12599-021-00726-8), omawia znaczący brak w literaturze na temat platform no-code w porównaniu ze stopniem zaawansowania dostępnych komercyjnie produktów.
Poniżej przedstawiono wybrane artykuły powiązane z tematyką tej pracy, z podziałem na tematykę.
- Porównanie istniejących platform
    - Low-Code Platform https://doi.org/10.1007/s12599-021-00726-8
    - Challenges & opportunities in low-code testing https://doi.org/10.1145/3417990.3420204
    - In Search of the Essence of Low-Code: An Exploratory Study of Seven Development Platforms https://doi.org/10.1109/MODELS-C53483.2021.00016
- Zastosowanie platform no-code 
    - Low-Code as Enabler of Digital Transformation in Manufacturing Industry https://doi.org/10.3390/app10010012
    - Modelling in low-code development: a multi-vocal systematic review https://doi.org/10.1007/s10270-021-00964-0
    - Low-code platform for automating business processes in manufacturing https://doi.org/10.1016/j.ifacol.2019.10.060
    - Building Smart Agriculture Applications Using Low-Code Tools: The Case for DisCoPar https://doi.org/10.1109/AFRICON51333.2021.9570936
    - Using Microsoft PowerApps, Mendix and OutSystems in Two Development Scenarios: An Experience Report https://doi.org/10.1109/MODELS-C53483.2021.00017
    - Modernized Application Development Using Optimized Low Code Platform
- Projektowanie platform no-code https://doi.org/10.1109/ASIANCON55314.2022.9908726
    - Low-Code Is Often High-Code, So We Must Design Low-Code Platforms to Enable Proper Software Engineering https://doi.org/10.1007/978-3-030-89159-6_14

Powyższy przegląd literatury wskazuje na problem poruszany również w artykule Low-Code Platform autorstwa Alexander C. Bock i Ulrich Frank: Platformy no-code, pomimo zainteresowania przemysłu, są tematem opisanym, na poziomie toerytycznym, powierzchownie.
Większość artykułów porównuje istniejące rozwiązania, oraz przedstawia przykłady użycia tych narzędzi.
Brakuje literatury opisującej teorytycznych podstaw konstruowania platform no-code, zapewniania poprawności wytwarzanego przez ich użytkowników oprogramowania, oraz jego utrzymwania.

## Plan pracy
Celem tej pracy jest zaadaptowanie narzędzi oraz technik występujących w tradycyjnej inżynierii oprogramowania, do programowania no-code, w sposób przystępny dla osób bez wykształcenia technicznego.
Proponowane rozwiązania będą powstawać w ramach platformy CasePro 8, następcy szeroko używanego w Polskiej bankowości CasePro 7.
W szczególności badane będą następujące obszary:
- Analiza statyczna zamodelowanej logiki i zapewnianie poprawności modelu. 
Podstawowym pytaniem badawczym będzie w tym aspekcie sprawdzenie, w jakim stopniu aplikacje no-code wymagają tworzenia dedykowanych narzędzi do weryfikacji.
W tym celu zbadana zostanie możliwość użycia analizatorów języka C# na modelu no-code przez generowanie ekwiwalentnego, ale niekompletnego, kodu C# na podstawie modelu procesu.
Taki program zostanie poddany analizie statycznej, używając kompilatora Roslyn, a znalezione diagnostyki zostaną odfiltrowane pod kątem adekwatności do oryginalnego procesu, oraz przetłumaczone na formę zrozumiałą dla programisty no-code.
- Automatyzacja testów powstałych aplikacji, przy użyciu sztucznej inteligencji.
- Przyśpieszanie tworzenia aplikacji, przez generowanie fragmentów modelu.
Zbadane zostanie zarówno zastosowanie prostych algorytmów herustycznych, pracujących na ręcznie przygotowanych szablonach jak i adaptacji Generatywnej Sztucznej Inteligencji (GSI).
Istotnym wyzwaniem do pokonania, przy wykorzystaniu GSI będzie brak dostępnych danych treningowych, specyficznych dla systemu CP8.
- Przyśpieszanie nauki wytwarzania aplikacji no-code.
Badanym zagadnieniem będzie wykorzystanie sztucznej inteligencji do wyjaśniania działania procesu bądź aktywności, w połączeniu z ręcznie przygotowaną biblioteką przykładowych modeli.
- Opracowanie mechanizmu modularyzacji i zarządzania zależnościami.
Platform no-code nie oferują łatwego sposobu dzielenia się gotowymi fragmentami modelu realizującymi określoną funkcjonalność.
Wszystkie współczesne języki programowania, dysponują narzędziami pozwalajacymi na dołączanie i zarządzanie zewnętrznymi zależnościami.
Praktyczne doświadczenie, wskazuje, że bardziej zaawansowanie użytkownicy platform no-code będą w stanie skorzystać z podobnego mechanizmu.
Wyzwaniem będzie zaprojektowanie zaprojektowanie go w sposób odpowiadający specyfice pracy z modelami no-code.

Najważniejszym aspektem tej pracy jest zapewnienie przystępności stworzonych narzędzi dla osób bez wykształcenia technicznego.
W tym celu, na obecnych użytkownikach platformy CasePro zostaną przeprowadzone badania sprawdzające zrozumienie diagnostyk, powszechność stosowania testów automatycznych oraz użyteczność automatycznie generowanego modelu.
Ponadto, konsturkcja języka w którym model aplikacji jest wyrażany, zostanie przeanalizowany pod kątem elementów promujących wytwarzanie poprawnych rozwiązań, bądź ich utrudniających.

W ramach tej pracy zostaną również uzupełnione wskazane w przeglądzie literatury braki w teorytycznych podstawach projektowania platform no-code.


## Współpraca pracodawcy z instytucjami edukacyjnymi/badawczymi

Zespół pracujący nad platformą CasePro, współpracował wcześniej z Narodowym Centrum Badań i Rozwoju.
W ramach tej współpracy poswstała platforma no-code Nova, stanowiąca podstawę dla CasePro 8.
W czasie pracy nad Nova, prowadzono badania użyteczności tworzonego rozwiązania, poprawności interfejsu użytkownika, oraz porównywano je z platformą CasePro 7.
