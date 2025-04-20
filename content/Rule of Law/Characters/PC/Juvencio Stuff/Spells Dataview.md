## Archmage Materia
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where materia = "Archimagus Materia"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```

## Medb de Llenyion
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where source = "Medb De Llenyion"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```

## Nevin Barley
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where source = "Nevin Barley"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```
## Infernal Spellbook
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where source = "Infernal Spellbook"
	Sort  level ASC, source ASC, school ASC, file.name ASC
```
## Alchemist Compendium (Not all learned)
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
		where source = "Alchemical Compendium" or learned = "Yes" and !materia
		and source != "Spellbook"
		Sort  level ASC, school ASC, file.name ASC
``` 
## Spellbook
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration", upcast as "Upcast"
	from #Spell 
	where source = "Spellbook"
	Sort  level ASC, school ASC, file.name ASC
``` 
## Alchemist Compendium (All learned)
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
		where source = "Alchemical Compendium" and learned = "No" and !materia
		Sort  level ASC, school ASC, file.name ASC
``` 

### All Spells
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration", upcast as "Upcast"
	from #Spell 
	Sort  level ASC, file.name ASC
``` 

### Not Learned Spells
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where learned = "No" 
	Sort  level ASC, school ASC, file.name ASC
``` 


# Test
```dataview
	Table without ID 
		file.link as "Spell", level as "Level", concentration as "Con", school as "School", castTime as 
		"C.T.", range as "Range", damage as "Dmg", components as "Comp.", duration as "Duration"
	from #Spell 
	where contains(school, "Divination")
	sort level ASC
``` 