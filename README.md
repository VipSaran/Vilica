<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Od nula do novog svjetskog poretka za 45 min ili kako brzo zapoceti doprinositi open source zajednici](#od-nula-do-novog-svjetskog-poretka-za-45-min-ili-kako-brzo-zapoceti-doprinositi-open-source-zajednici)
  - [Uvod](#uvod)
    - [Github](#github)
      - [Open source licence](#open-source-licence)
      - [Markdown](#markdown)
  - [Kako doprinijeti open sourceu](#kako-doprinijeti-open-sourceu)
    - [Pull request](#pull-request)
      - [Step 1: Forkanje upstream repozitorija](#step-1-forkanje-upstream-repozitorija)
      - [Step 2: Kloniranje forkanog repozitorija](#step-2-kloniranje-forkanog-repozitorija)
        - [Drzanje forkanog repozitorija u syncu](#drzanje-forkanog-repozitorija-u-syncu)
      - [Step 3: Izmjena sadrzaja](#step-3-izmjena-sadrzaja)
      - [Step 4: Kreiranje pull requesta](#step-4-kreiranje-pull-requesta)
  - [Sto dalje?](#sto-dalje)
  - [Hintovi](#hintovi)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Od nula do novog svjetskog poretka za 45 min ili kako brzo zapoceti doprinositi open source zajednici

## Uvod

Moj standardni workflow: zapocinjem rad na nekom projektu i smisljam arhitekturu. Ovdje, naravno, ne evaluiram samo procese potrebne da se dobije zeljeno rjesenje, vec i najbolju tehnologiju za rjesavanje problema, a pri tome gledam da bootstrapam pojedine segmente sto vise mogu, a to radim tako da koristim gotova, stabilna, popularna i (po mogucnosti) dobro dokumentirana rjesenja. O, da, i obavezno besplatna! :)

Tu u pricu uskace open source.

Primjeri open source librarija koje koristim su mnogobrojni, no nema smisla da ih navodim jer se vezu za moje interese odn. za projekte na kojima ih koristim.

Iako se godinama open source dokazivao kao odlican nacin za razvoj relevantnog i stabilnog softvera, isto tako se nije mogao cijepiti protiv onoga od cega ni jedan software nije cijepljen -- bugova. Tako sam i ja kroz koristenje tih OS librarija vremenom nailazio na nedostatke u njima. E, sada, ako je nedostatak blokirajuci odn. ako zbog tog buga ne mogu ostvariti zeljenu funkcionalnost, skuzio sam da imam 3 opcije:

1. naci drugi library koji radi isto (vidi kriterije gore),
2. prijaviti bug i cekati da ga netko popravi,
3. popraviti bug sam.

Manje-vise, ove su tri opcije zapravo evolucija pripadanja open source zajednici kroz prihvacanje odgovornosti.
Kako se kaze, "ono si sto jedes", isto tako bi se moglo i reci da ako je OS software svaciji onda je i tvoj, a ako je nesto tvoje, onda prema tome imas i odgovornosti, ako nikakve druge, onda drustvene odgovornosti -- da vratis bar koliko si od drugih i dobio.

Cilj je ovoga tecaja proci kroz mogucnosti vracanja zajednici i olaksati nacin koji je nama (programerima) naj prirodniji -- doprinos koodu.

### Github

Github je odabran kao radna platforma jer je daleko najpopularniji servis za hostanje open sourcea, a samim time je najvjerojatnije da se svatko od nas susreo s bar jednim OS projektom koji se razvija uz njegovu pomoc.

Glavna nacela Githuba, a koja njegovi toolovi i workflow potpomazu i omogucuju, su:

- transparentnost (software dostupan, proces kreiranja vidljiv, komunikacija bez zapreka)
- sudjelovanje (bez izoliranja do dijeljenih ciljeva),
- suradnja (kad se maknu prepreke, suradnja cvjeta).

#### Open source licence

Postoji mnogo varijanti, a najlakse je odgovarajucu odabrati pomocu [ChooseALicense.com](http://choosealicense.com/).

Ukratko;

- MIT --> mijenjaj sto hoces, no ostavi mene kao originalnog autora i nemoj me drzati odgovornim
- Apache --> kao MIT, no daje patentna prava korisnicima
- GPL --> tko god mijenja, kood mora napraviti dostupnim na isti nacin
- CreativeCommons --> za dokumente, slike

Licencu nije neophodno odabrati!!

*[Procitaj](https://github.com/blog/1530-choosing-an-open-source-license) vise o tome.*

#### Markdown

Sto je Markdown?

To je markup jezik sa sintaksa za formatiranje kroz obican (plain) tekst koji se kroz tool pretvara u HTML. Prednosti su sto je citljiv, dopusta pisanje rich text sintakse preko obicnog teksta/editora.

[Primjer](https://en.wikipedia.org/wiki/Markdown#Example) pokazuje odnos izvornog kooda/texta prevedenog u HTML i prikazanog u browseru.

Github koristi nekoliko svojih specificnosti vezanih uz jezik.

*[Procitaj](https://help.github.com/articles/github-flavored-markdown/) vise o tome.*

## Kako doprinijeti open sourceu

- donacije,
- moderiranje foruma,
- izrada web stranice,
- prijava issua/buga,
- prijedlog featura,
- dopuna/izmjena sadrzaja kroz pull request

### Pull request

Pull requests ti omogucuje da drugima kazes o izmjenama koje si pushao na Github repo. Jednom kada se pull request posalje, zainteresirane strane mogu reviewirati izmjene, diskutirati potencijalne promjene i cak pushati naknadne commitove ako je potrebno.

Da bi se doslo da mozemo napraviti pull request, potrebno je nekoliko radnji prvo odraditi.

#### Step 1: Forkanje upstream repozitorija

Upstream (odn. originalni) repozitorij je uobicajeno postavljen tako da samo nekoliko ljudi (tj. moderatora) ima commit prava, a da svi ostali za svoje izmjene prvo salju prijedlog odn. "pull request".

Posto upstream repo ima efektivno samo read-only prava, izmjene moramo prvo napraviti u nekom repozitoriju u kojem imamo i write prava a to je samo repozitorij gdje smo mi vlasnik (nije samo, no u ovom kontekstu je!).

1. odemo do repozitorija ([https://github.com/VipSaran/Vilica](https://github.com/VipSaran/Vilica)) koji zelimo forkati,
2. kliknemo na Fork button:

![fork_button](https://help.github.com/assets/images/help/repository/fork_button.jpg)

To je to. Sada u svom privatnom prostoru na Githubu imamo kopiju projekta kojemu zelimo doprinijeti.

*[Procitaj](https://help.github.com/articles/fork-a-repo/) vise o tome.*

#### Step 2: Kloniranje forkanog repozitorija

Da bi mogli napravili zeljene izmjene, trebamo taj forkani repo povuci lokalno -- kloniranjem:

    git clone https://github.com/YOUR-USERNAME/Vilica


##### Drzanje forkanog repozitorija u syncu

Kako bi bili up-to-date sa izmjenama na upstreamu (a sto ce na kraju, ukoliko code base bude sto slicniji, olaksati merge naseg pull requesta), potrebno je s vremena na vrijeme uskladiti nas repozitorij (lokalni i forkani) s upstreamom. To se radi na slijececi nacin:

1. unutar lokalnog repoa dodati upstream `git remote add upstream https://github.com/VipSaran/Vilica`,
2. povuci izmjene `git fetch upstream`,
3. posto u svom repou mozemo raditi u bilo kojem branchu, potrebno je napraviti `git checkout master`,
4. uvrstiti izmjene u nas repo sa `git merge upstream/master`,
5. gurnuti izmjene na nas fork sa `git push origin`.

*[Procitaj](https://help.github.com/articles/fork-a-repo/#step-3-configure-git-to-sync-your-fork-with-the-original-spoon-knife-repository) vise o tome.*

#### Step 3: Izmjena sadrzaja

    while(!fixed) {
      fix();
      fixed = test();
    }

    commit();
    push();

#### Step 4: Kreiranje pull requesta

Kako smo u proslom koraku izmjene koje smo radili lokalno vec pushali na origin (odn. na forkani repozitorij, sa `git push origin`), kreiranje pull requesta nastavljamo tamo -- na Githubu.

1. otici na `https://github.com/YOUR-USERNAME/Vilica`,
2. kliknuti na "Compare & review" gumb:
        ![compare_and_review](https://help.github.com/assets/images/help/pull_requests/pull-request-start-review-button.png)
3. razmotriti razlike,
4. zapoceti kreiranje pull requesta klikom na gumb:
        ![start_pull_request](https://help.github.com/assets/images/help/pull_requests/pull-request-review-create.png)
5. upisati naziv i komentrirati (ako je potrebno), te kreirati pull request klikom na gumb:
        ![create_pull_request](https://help.github.com/assets/images/help/pull_requests/send-pull-request.png)

Moguce daljnje akcije su eventualna diskusija u threadu tog pull requesta (uz mogucnost potrebnih dopuna).

*[Procitaj](https://help.github.com/articles/using-pull-requests/) vise o tome.*

## Sto dalje?

Koristite open source sto vise, postujte trud drugih i ne ustrucavajte se zajednici uzvratiti uslugu!


## Hintovi

- ne re-formatirati kood --> nitko ga nece htjeti povuci jer se ne vide stvarne izmjene
- ne ubacivati funkcionalnost koja nije pokrivena pull requestom