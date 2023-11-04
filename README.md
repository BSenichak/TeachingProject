# Teaching Project for group SB16 Web middle

# My name is Bohdan

![my img](https://images2.minutemediacdn.com/image/upload/c_crop,h_1193,w_2121,x_0,y_64/f_auto,q_auto,w_1100/v1565279671/shape/mentalfloss/578211-gettyimages-542930526.jpg)

I'm **JavaScript developer**. *This is my example of code:*

```javascript
document.getElementById("filter-form").addEventListener("submit", function(event){
    event.preventDefault();
    sortedPokemons = pokemons
    if(event.target["name-filter"].value){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.name.indexOf(event.target["name-filter"].value.toLowerCase()) != -1
        })
    }
    if(event.target["hp-filter-form"].value > 10){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[0].base_stat >= event.target["hp-filter-form"].value
        })
    }
    if(event.target["hp-filter-to"].value < 250){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[0].base_stat <= event.target["hp-filter-to"].value
        })
    }
    if(event.target["attack-filter-form"].value > 5){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[1].base_stat >= event.target["attack-filter-form"].value
        })
    }
    if(event.target["attack-filter-to"].value < 130){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[1].base_stat <= event.target["attack-filter-to"].value
        })
    }
    if(event.target["defence-filter-form"].value > 5){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[2].base_stat >= event.target["defence-filter-form"].value
        })
    }
    if(event.target["defence-filter-to"].value < 180){
        sortedPokemons = sortedPokemons.filter((pokemon)=>{
            return pokemon.stats[2].base_stat <= event.target["defence-filter-to"].value
        })
    }
    event.target['types'].forEach(function(filterType){
        if(!filterType.checked){
            sortedPokemons = sortedPokemons.filter(function(pokemon){
                for(let i in pokemon.types){
                    if(pokemon.types[i].type.name == filterType.value) return false
                }
                return true
            })
        }
    })
    reddrawSortPokemons();
})
```

My social links
* [my instagram](http://instagram.com)
* [my telegram](http://t.me/badyasik)
