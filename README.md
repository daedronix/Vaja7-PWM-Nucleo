# Vaja7-PWM-Nucleo
<h4> V levem Pinout oknu razširite nabor možnosti za Timers ter časocnik TIM1. Clock Source nastavite kot internal clock. Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? </h4>
<p> Omogočili smo PA8. Poleg pina se izpiše TIM1_CH1. </p>
<h4> V Clock Configuration kliknemo za TIM1 vrednost Prescaler v zavihku Counter settings določite tako, da bo časovnik delal s frekvenco 1MHz. Koliko je vrednost Prescaler? </h4>
<p> Vrednost Prescaler je 16 </p>
<h4> Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša sedaj? </h4>
<p> 10kHz. </p>
<h4> V PWM Generation Channel nastavite pulse na 50. Kaj pomeni ta parameter? </h4>
<p> S tem parametrom nastavimo vrednost širine pulza </p>
<h4> Poiščite prenastavljeni parameter Pulse (ki je 50) v vaši kodi in prepišite ukaz, ki ga je generiral CubeMX: </h4>
<p> sConfigOC.Pulse = 50; </p>
<h4> V kodi spremenite vrednost širine pulza na 25%. Zapišite popravljeni ukaz v kodi: </h4>
<p> sConfigOC.Pulse = 25; </p>
<h4> Zapišite kaj počnejo ukazi v 1., 2. in 3. vrstici (v user code begin 3) </h4>
<p> Na začetku zanke program nastavi htim1.Instance->CCR1 na vrednost spremenljivke dutyCycle. </p>
<p> Vsakič ko program "loop-a" skozi to vrstico doda spremenljivki dutyCycle + 10. </p>
<p> Pogleda če je vrednost dutyCycle-a večja od 90 in nastavi dutyCycle nazaj na 10, kar pomeni da je neskončna zanka. </p>

<h4> Komentar </h4>
<p> Nastavljamo širino pulza in hitrost frekvence. Pri izdelavi sva imela probleme z delovanjem, ker nam koda ni delovala. To sva popravila tako, da sva še enkrat generirala kodo. </p>
