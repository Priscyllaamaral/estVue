# estVue
alguns exemplos de código usando vueJs e Vuetify


## v-slot:activator="{ on }"
### ele vai "escutar" quando o mouse passar sobre o elemento e vai fazer uma ação

## v-bind
### ele vai alterar o as propriedades de uma tag html



    <div id=app>
        <input v-bind:value="name"></input>
        <v-data-table :headers="h" :items="i">
            <template v-slot:item="{ item }">
                <tr>
                    <td>{{ item.id }}</td>
                    <td> {{ item.nome }}</td>
                    <td>
                        <v-tooltip bottom>
                          <template v-slot:activator="{ on, attrs }">
                              <v-btn v-on="on"> Passar o mouse </v-btn>
                          </template>
                          <h1 v-bind:style="{'color': cor}" >Passou</h1>
                        </v-tooltip>
                    </td>
                 </tr>
             </template>
       </v-data-table>
   </div>
 
 
 
 
  new Vue({
  el: '#app',
  vuetify: new Vuetify(),
  data: () => ({
    name:"aqui",
    cor:'red',
    show: false,
    h :[{title:'ID', key:'id'},{title:'Name', key:'nome'}],
    i : [{'id':1, nome:'pri'},{'id':2, nome:'sam'},{'id':3, nome:'ger'},{'id':4, nome:'aqui'},{'id':5, nome:'gabi'}], 
  }),
})






<v-menu>
   <template v-slot:activator="{ on }">
      <v-btn v-on="on"> Dropdown </v-btn>
   </template>
        <v-list>
          <v-list-item v-for="index in 4" :key="index">
            <v-list-item-title>Item {{ index }}</v-list-item-title>
          </v-list-item>
        </v-list>
</v-menu>

