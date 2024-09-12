# Reflektion om implementering af figma design:

Som opstart på denne opgave var jeg syg, som gjorde at jeg synes at starten var lidt op ad bakke. Samtidig endte denne opagve med at være en ret stor motivation for at komme i gang og se tilbage på det undervisning jeg havde misset.

Jeg startede opgaven ved at lave et komponent af gangen, og dermed dele opgaven op i mere "spiselige" bidder. I forbindelse med det, har jeg særligt haft fokus på at bruge Astro's mulighed for at lave komponenter så meget som muligt. Hvor jeg normalt ville have tendens til at lave flere komponener eller måske struggle lidt med props og at ændre i komponeneter, synes jeg at jeg har fået en meget bedre forståelse af dette.
_Eksempel nedenfor:_

```javascript
---
const { text, color } = Astro.props;
---

<button class={color}>{text}</button>
```

```css
/* Classnames for different color variants */
.primary {
  background-color: var(--primary-color);
  color: var(--action-text-color);
}

.secondary {
  background-color: var(--secondary-color-shade);
  color: var(--secondary-text-color);
}

.action {
  background-color: var(--action-color);
  color: var(--action-text-color);
}
```

En aha oplevelse som jeg synes jeg havde med denne opgave, var at gøre brug af endnu flere selectore og pseudo selectorer, bl.a. :not(), :nth-child() osv. Derudover har jeg også haft brug nesting ret meget især til at style direkte børn, som er nyt for mig. Begge disse dele synes jeg er super smart og en god måde at style specifikke elementer, uden at gøre brug af classnames eller id'er.
Derudover synes jeg også at det har været spændende at lære hvordan man kan benytte container queries i stedet for media queries. Det vil jeg helt sikkert bruge mere tid på at lære. _Eksempel nedenfor:_

```css
& p:not(:last-child) {
  margin-bottom: var(--spacing-l);
}

& > * {
  margin-right: var(--spacing-3xl);
}

& :nth-child(2) {
  width: 260px;
  height: 260px;
  top: 150px;
  left: -100px;
}
```

I forbindelse med den undervisning jeg havde misset, synes jeg at der var en del elementer som jeg havde svært ved, ved opgaven. Jeg nåede bl.a. aldrig til at lave scrolling-container sektionen, da jeg havde svært ved at forstå hvordan det skulle gøres. Jeg havde brugt en del tid på at lave de øvelser som var tilknyttet, og dermed valgte jeg til sidst at komme videre og ville vende tilbage hvis jeg havde tiden.
Derudover synes jeg også at de forskellige mønstre som var bag diverse elementer har været særligt besværlige at have med at gøre. Nemlig da de skulle se ud på en bestemt måde på pc, men også se godt ud responsivt. Det synes jeg nok er noget jeg har brugt lidt for meget tid på, fremfor nogle andre elementer. _Eksempeler nedenfor_
![Alt text](/docs/excample-1.png)
![Alt text](/docs/excample-2.png)

En tredje svær ting ved denne opgave var at designet kun var til pc. Vi har generelt haft meget fokus på altid at designe og kode mobile first, så det gjorde jeg selvfølgelig også denne gang, men det synes jeg også har skabt nogle bump på vejen. Nemlig da jeg har skulle tage udgangspunkt i pc designet. Så hvis jeg skulle gøre det om, havde jeg nok ikke kodet dette sitet mobile first.

Alt i alt synes jeg at det har været en super spændende og udfordrende opgave og at jeg har lært nogle brugbare css styling tips, som jeg vil tage med videre til de kommende forløb.
