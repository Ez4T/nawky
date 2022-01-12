<template>
  <div class="about my-6">
    <h1 class="text-6xl text-gray-1000">This is a Leaderboard page</h1>
      <TabsWrapper>
        <Tab title="Tab1">Hello from Tab1</Tab>
        <Tab title="Tab2">Hello from Tab2</Tab>
        <Tab title="Tab3">Hello from Tab3</Tab>
        <Tab title="Tab4">Hello from Tab4</Tab>
      </TabsWrapper>
    <div class="container flex justify-center mx-auto mt-6">
      <div class="flex flex-col">
        <div class="w-full">
          <div class="border-b border-gray-200 shadow">
            <table>
              <thead class="bg-grey-50">
                <tr class="whitespace-nowrap">
                  <td class="px-6 py-2 text-3xl text-gray-500">Rank</td>
                  <td class="px-6 py-2 text-3xl text-gray-500">Name</td>
                  <td class="px-6 py-2 text-3xl text-gray-500">Point</td>
                </tr>
              </thead>
              <tbody class="bg-white">
                <tr
                  class="whitespace-nowrap"
                  v-for="(item, index) in users"
                  :key="index"
                >
                  <td class="px-6 py-4 text-xl text-gray-500">{{ item.ID }}</td>
                  <td class="text-xl text-gray-900">{{ item.Name }}</td>
                  <td class="text-xl text-gray-900">{{ item.Surname }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import TabsWrapper from "../components/TabsWrapper.vue";
import Tab from "../components/Tab.vue";
export default {
  name: "Leaderboard",
  data() {
    return {
      users: {},
      numberOfUsers: 0,
    };
  },
  async created() {
    const getUserData = await axios
      .get("https://sheet2api.com/v1/9OLQUnxSrqmQ/vue-sheets")
      .then((response) => (this.users = response.data));
    this.users = getUserData;
  },
};
</script>

<style scoped></style>
