<template>
  <div>
    <div>
      <button
        @click="
          filter = entry;
          active = index;
        "
      >
        {{ position.role }}
      </button>
    </div>
    <section>
      <Profile
        v-for="profile in profiles"
        :key="profile.id"
        :profile="profile"
        />
    </section>
  </div>
</template>

<script>
export default {
  name: "DataDisplay",
  data: function() {
    return {
      fkey: "role",
      filterList: ["Frontend", "Backend"],
      filter: "All",
      profiles: []
    };
  },
  methods: {
    resultsFilter(entry) {
      if (this.filter !== "All") {
        if (entry[this.fkey] === this.filter) {
          return entry;
        }
      } else {
        return entry;
      }
    }
  }
};
