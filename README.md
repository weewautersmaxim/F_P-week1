# Emoji oefening

## User Stories

- [ ] Als gebruiker kan ik alle emojis bekijken.
- [ ] Als gebruiker kan ik bij hover de shortcode van een emoji zien.
- [ ] Als gebruiker kan ik bij hover een emoji toevoegen aan favorieten.
- [ ] Als gebruiker kan ik de website responsive gebruiken.
- [ ] Als gebruiker kan ik bij het opnieuw bezoeken van de website nog steeds mijn favorieten zien.
- [ ] Als gebruiker kan ik het totaal aantal favorieten zien.
- [ ] Als gebruiker kan ik een lijst met mijn favoriete emojis zien.
- [ ] Als gebruiker kan ik na het klikken op een `:emoji:` die naam plakken als tekst (waar dan ook).
- [ ] Als gebruiker zie ik een rood bolletje bij elke emoji die ik als favoriet toegevoegd heb.

## Design

Zie screenshots (`/design`) voor design.

## Assets & colors

- De kleur van de rode circle is `bg-red-500`.
- De achtergrond is `bg-gray-50`.

## Technical

- Gebruik een vuex-store om favorieten bij te houden. Probeer op een goede manier met typescript te werken.

  - Gebruik een enum voor de namen van de functies die je in de store hebt (zowel in de mutations als in de getters), bv.:

    ```typescript
    mutations: {
      [MutationTypes.TOGGLE_FAVORITE](state: State, e: Emoji) {
        ...
      }
    }
    ```

    ```typescript
    getters: {
      [GetterTypes.CHECK_FAVORITE]: (state: State) => (eName: string) =>
        ...
    }
    ```

  - Gebruik modules (in dit geval 1).
  - Dit wil ik ook goed samen met jullie doen, veel is een kwestie van uitzoeken, dat heb ik al gedaan op voorhand.

- We hebben zowel de keys als de values nodig in ons object!
- Veel komt in dit labo neer op eenvoudige data-binding in combinatie met de vuex-store, werken met TailwindCSS & de composition API.

## Uitbreiding

- [ ] Voorzie een melding dat een 'copy' geslaagd is.
- [ ] Voorzie een zoek-functie.
