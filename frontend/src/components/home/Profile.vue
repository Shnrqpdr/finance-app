<template>
  <div>
    <v-list>
      <v-list-item two-line class="px-2">
        <v-list-item-avatar>
          <img src="https://randomuser.me/api/portraits/women/81.jpg" />
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Jane Smith</v-list-item-title>
          <v-list-item-subtitle>Logged In</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <v-divider></v-divider>
    <v-list nav dense>
      <v-list-item-group v-model="selectedItem" color="primary">
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </div>
</template>
<script>
export default {
  name: "ProfilePage",
  data() {
    return {
      selectedItem: 0,
      items: [
        { text: "Minha conta", icon: "mdi-account" },
        { text: "Minha renda", icon: "mdi-account-cash" },
        { text: "Estatísticas", icon: "mdi-chart-scatter-plot" },
      ],
    };
  },
};
</script>
