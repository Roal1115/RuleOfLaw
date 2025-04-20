### All prepared Spells (all sourcers)
```dataview
	Table without ID 
		file.link as "Spell Name", level as "Level", concentration as "Con", castTime as "C.T.", range as "Range", duration as "Duration", damage as Dmg, Ritual, school as Magic, upcast as Upcast, components as Components
	from #Spell 
	where Ritual = "Yes" or materia or source = "Feature" or prepared = "y"
	Sort  level ASC, file.name ASC, school ASC
```

### Ritual
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", castTime as "C.T.", range as "Range", duration as "Duration", school as Magic  
	from #Spell 
	where Ritual = "Yes"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```
### Feature Magic
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", castTime as "C.T.", range as "Range", duration as "Duration", school as Magic 
	from #Spell 
	where source = "Feature"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```
### [[Archmage Materia]], [[Blue Materia]] e Items Magicos
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", castTime as "C.T.", range as "Range", duration as "Duration", damage as Dmg, school as Magic 
	from #Spell 
	where materia
	Sort  level ASC, source ASC, school ASC, file.name ASC
```

### Wizard Prepared = Int + Wizard Lvl
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", castTime as "C.T.", range as "Range", duration as "Duration", school as Magic
	from #Spell 
	where prepared = "y" and !materia and source != "Feature"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```

