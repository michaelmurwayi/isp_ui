<template>
    <v-app>

     <form >

                <v-list-item class="mt-n2">
                    <v-text-field label="Firstname"  placeholder= "firstname" min="10" ></v-text-field>
                  </v-list-item>
                <v-list-item class="mt-n5">
                    <v-text-field label="Surname" placeholder= "surname"></v-text-field>
                  </v-list-item>
                <v-list-item class="mt-n5">
                    <v-text-field label="Email" placeholder= "email"></v-text-field> 
                  </v-list-item>
                <v-list-item class="mt-n5">
                    <p class=" mt-4 mr-2 cyan--text text--darken-1">UserId:</p>
                    <v-list-item-subtitle>2 times in a day before food</v-list-item-subtitle>
                  </v-list-item>
                <v-btn
                  class="mx-2 mr-n10"
                  fab
                  dark
                  large
                  color="cyan"
                  style="position:relative; left:220px; bottom:10px;"
                >
                  <v-icon dark>
                    mdi-pencil
                  </v-icon>
                  Edit
                </v-btn> 
                </form>
    </v-app>

</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>

</style>