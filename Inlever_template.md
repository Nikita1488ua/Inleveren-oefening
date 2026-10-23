# Mini-level — Inleveren

**Naam:** Nikita
**Klas:** SD1B
**Datum:** 23.20.3036 
**Les:** GDV Les 6

---

## Wat heb ik gemaakt?

Dit is een mini level waar moet je alle coins collecten.

## Screenshot / GIF van je level

<!-- Voeg hieronder een screenshot of een GIF toe van je werkende level.
     Sleep het bestand naar deze map en gebruik dan de syntax hieronder. -->

![Mini-level preview](C:\Users\vika_\Documents\MA\Bewijzenmap\periode 1.1\unit 1\GD\Video.gif)

<!-- Tip: gebruik ShareX, LICEcap of de ingebouwde Xbox Game Bar (Win+G) om een GIF op te nemen. -->


## Bewegend object

<!-- Welk object beweegt en hoe heb je dat gedaan? -->
Player

```csharp
// Plak hier het script of het stuk code dat het object laat bewegen.
void Update()
{
  float horizontal = Input.GetAxis("Horizontal");
  float vertical = Input.GetAxis("Vertical");

  Vector3 movement = new Vector3(horizontal, 0f, vertical);

  transform.Translate(movement * speed * Time.deltaTime);
}
```


## Collider of trigger

<!-- Welk object heeft een collider of trigger, en wat gebeurt er? -->

...

```csharp
// Plak hier de OnCollisionEnter/OnTriggerEnter code die je hebt gebruikt.
private void OnTriggerEnter(Collider other)
{
 PlayerController player = other.GetComponent<PlayerController>();

 if (player.health < player.MaxHealth)
 {
     player.health +=1;

     Debug.Log("Health: " + player.health);

     Destroy(gameObject);
 }
 else
 {
     Debug.Log("You already have max health!");
 }
}
```
Als de speler raakt een munt krijgt hij 1 point health

## Logica met `if` of `switch`

<!-- Beschrijf kort welke keuze je hebt gemaakt (bijv. sleutel → deur open). -->

...

```csharp
// Plak hier het stuk code met jouw if- of switch-logica.
if ()
{
     health = MaxHealth;
     Debug.Log("You win!");
}
```

Alse alle muntjes collect jij win.

## Eigen extra idee

<!-- Wat is jouw eigen extra feature? Beschrijf wat het doet en hoe je het hebt gebouwd. -->

...

```csharp
// Optioneel: plak hier de bijbehorende code.

```
Ik geef textures naar player en coins, camera gaat met de speler samen.


## Evaluatie

### Wat ging goed? en waarom?

<!-- Wat lukte je makkelijk of waar ben je trots op? -->

...
Alles ging goed.

### Wat vond je lastig? en waarom?

<!-- Waar liep je tegenaan? Hoe heb je het opgelost (of niet)? -->

...
Camera zetten

### Wat zou je een volgende keer anders doen?

<!-- Wat heb je geleerd? -->

...
