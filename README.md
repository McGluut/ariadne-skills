# Ariadne Skills

**Karteren** maakt een kaart van een document of project. Je kunt vanuit een bewering teruggaan naar de bron, zien welk bewijs ontbreekt en bepalen welke vraag je als eerste moet uitzoeken.

In het [voorbeeld van een energiemeting](.agents/skills/karteren/references/example-projectbrief.md) overweegt een werkplaats apparatuur te vervangen. De kaart wijst naar de regel met het besliscriterium: twee vergelijkbare metingen. De bijlage met de waarden ontbreekt. Zo zie je precies wat je nodig hebt om over vervanging te beslissen.

## Geef deze opdracht aan je agent

```text
Gebruik Karteren uit https://github.com/McGluut/ariadne-skills op het document dat ik aanlever. Begin met een korte kaart. Laat me bij één bewering inzoomen op de bron en wijs aan welk ontbrekend bewijs mijn besluit kan veranderen.
```

De [skillinstructies](.agents/skills/karteren/SKILL.md) en het [startpunt voor agents](AGENTS.md) zijn ook rechtstreeks te openen. Je kunt de eerste opdracht uitproberen op de drie genummerde bronregels in het voorbeeld.

<details>
<summary>Karteren gebruiken in Codex en Codex CLI</summary>

Kloon de repo en open de map als project in Codex. Voor de CLI:

```sh
git clone https://github.com/McGluut/ariadne-skills.git
cd ariadne-skills
codex
```

Typ in de nieuwe sessie `$karteren` en geef een bron en je vraag mee. Om de skill in een ander project te gebruiken, kopieer je de hele map `.agents/skills/karteren/` naar dezelfde plek in dat project. Als daar al een versie staat, vergelijk ze eerst.

Een agent met leestoegang tot GitHub kan de [werkwijze](.agents/skills/karteren/SKILL.md) ook direct volgen en de twee bijbehorende referenties openen. Je kiest zelf welke bron je vervolgens aan je agent geeft.

</details>

<details>
<summary>Wat de agent oplevert en hoe je het controleert</summary>

Een kaart bevat beweringen, bronplaatsen en relaties. Vraag bijvoorbeeld: *Op welke bronregel rust dit besluit?* Volg één verwijzing zelf. Bij een ontbrekend stuk vermeldt de kaart welke gevolgtrekking openblijft. Bij delen kiest de agent alleen bronnen die de ontvanger mag zien. Het [manifestformaat](.agents/skills/karteren/references/map-spec.md) beschrijft die informatie voor een agent die de kaart verder verwerkt.

</details>

[Gebruiksvoorwaarden](LICENSE.md)
