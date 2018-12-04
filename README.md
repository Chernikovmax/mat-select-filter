# mat-select-filter

## Github
https://github.com/mdlivingston

## Description

The mat-select-filter is a filterer for the material select drop downs. They currently do not support this so I decided to make my own. 

## Install 

#### npm

```
$ npm install mat-select-filter
```

## How to use

Be sure to import into desired module: 

```
import { MatSelectFilterModule } from 'mat-select-filter';
```

Next just add it to the desired material select: 

```
<mat-form-field color="accent">
  <mat-select #select [value]="selectedVariableName" placeholder="{{ placeholder }}">
    <mat-select-filter [array]="variables" (filterArrayReturn)="filteredVariables = $event"></mat-select-filter>
    <mat-option>
      Hey, I love you. <3
    </mat-option>
  </mat-select>
</mat-form-field>
```

Send your desired filtered array using the [array]="variables" or [array]="['one', 'two', 'three']"...

The (filterArrayReturn) method returns the filtered results after every keyboard action while searching... 

The placeholder text for the search box is access by:

```
<mat-select-filter [placeholder]="'Search..'" [array]="variables" (filterArrayReturn)="filteredVariables = $event"></mat-select-filter>
```

