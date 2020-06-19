# TEST---PYTHON-SUMMER-INTERN
Pokud nebudete vědět jak něco 'rozběhnout' nebo nepochopíte proč jsem něco udělal tak, jak jsem to udělal, je velká šance, že to bude někde tady napsané, pokud ne, zeptejte se mě.
Jsou tu totiž dvě možnosti, jak tuto aplikaci 'rozběhnout'.
# 1A) Aplikace s Flask frameworkem
Na tuto možnost je vše připravené. Tedy až na databázi(o té si povíme níže).
Takže, nejdříve vysvětlím, jak jsem to udělal a hlavně z jakého důvodu jsou některé věci tak, jak jsou. 
Ze všeho nejdřív si asi budete říkat: 'Proč používá Pymongo a Flask' odděleně a nepoužívá přímo flask-pymongo.
No.. Je to proto, protože jsem do 3/4 projektu nevěděl, že něco takového existuje.
Dále si asi řekenete: 'Proč nepoužívá mongo databázi přímo jako output pro stránku, ale používá seznamy, z kterých pak udělá JSON.'
Nevím, jak, to je ten důvod:D. Data se ukládájí jak do proměnných seznamů(ty ukládájí pouze posledních 50otázek), tak do mongo databáze(ta ukládá úplně všechno).
Tak, a teď jedna chyba, kterou jsem nedokázal opravit. Když si na stránce rozkliknete 50 posledních otázek, pak bez restartu serveru půjdete zpět a rozkliknete N tagů větších než 15 znaků, na stránce se sice všechno zobrazí normálně, ale v mongo databázi už ne. Tu chybu musíte vidět sama, abyste pochopila.
# 1B) Jak rozběhnout mongo databázi a Flask server?
Začneme se 'setupem' mongo databáze. V kódu je databáze nastavená na localhost na portu 27017. Pokud máte jiný server mongodb nebo cokoliv v kódu jsou komentáře, které ukazují, kde můžete změnit mongodb server(přesněji v 'app.py' a v 'stack/stack/pipelines.py' (ale to už je pro něco jiného, o čemž si povíme níže)
Pokud nemáte mongodb a potřebujete nějak pomoc, napište nebo zavolejte.
Teď stačí pouze spustit server (napsat 'python app.py' ve složce, kde je app.py)
# 2A) Aplikace BEZ Flask frameworku
V stack/stack máte soubor pipelines, tam je ale komentářů, že? Pokud chcete aplikaci rozběhnout, řiďte se podle nich.