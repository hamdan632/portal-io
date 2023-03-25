<template>
  <v-container>
    <v-card class="mb-3">
      <v-card-title>Your Wallet</v-card-title>
      <v-card-text>
        <v-tabs v-model="tab">
          <v-tab v-for="tab in tabs" :key="tab">
            {{ tab }}
          </v-tab>
          <v-tab-item v-for="(tab, index) in tabs" :key="tab" :value="index">
            <v-card v-if="tab === 'Portfolio'">
              <v-card-text>
                <v-card class="mb-3">
                  <v-btn icon color="primary">
                    <v-icon>mdi-plus</v-icon>
                  </v-btn>
                  <div>Add Payment Method</div>
                </v-card>
                <!-- add your portfolio content here -->
              </v-card-text>
            </v-card>
            <v-card v-if="tab === 'Transactions'">
              <v-card-title>Transactions</v-card-title>
              <v-card-text>
                <!-- add your transactions content here -->
              </v-card-text>
            </v-card>
            <v-card v-if="tab === 'Inventory'">
              <v-card-title>Inventory</v-card-title>
              <v-card-text>
                <!-- add your inventory content here -->
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  layout: 'detailsPage',
  data() {
    return {
      tab: 0,
      tabs: ["Portfolio", "Transactions", "Inventory"]
    };
  }
};
</script>

<style>
/* add your custom styles here */
</style>
