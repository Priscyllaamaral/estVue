# estVue
alguns exemplos de código usando vueJs e Vuetify


## v-slot:activator="{ on }"
### ele vai "escutar" quando o mouse passar sobre o elemento e vai fazer uma ação

## v-bind
### ele vai alterar o as propriedades de uma tag html




                  <v-tooltip bottom>
                      <template v-slot:activator="{ on }">
                            <v-btn v-on="on"> Passar o mouse </v-btn>
                      </template>
                      <h1 v-bind:style="{'color': cor}"> Passou </h1> 
                  </v-tooltip>

