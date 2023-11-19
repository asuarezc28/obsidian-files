<button mat-icon-button (click)="toggleFavorite()" [ngClass]="{'favorite': isFavorite}">
  <mat-icon>favorite</mat-icon>
</button>
En este ejemplo, toggleFavorite() es una función en tu componente que cambia el estado de la variable isFavorite. Cuando isFavorite es true, se agrega la clase CSS favorite al botón, lo que cambia el color del icono a rojo. Cuando isFavorite es false, la clase se elimina y el color del icono vuelve a su estado original.

Espero que esto te ayude. ¡Avísame si tienes alguna otra pregunta!