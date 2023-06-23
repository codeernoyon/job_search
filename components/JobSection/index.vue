<template>
  <div class="min-h-screen w-full container m-auto px-3">
    <!-- items -->
    <div class="text-main-clr" v-for="{ da, index } in data">
      <JobSectionJobItems :itemData="da" :index="index" />
    </div>
    <!-- pop up -->
    <PopUp />
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          title: "Need Web Developer",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit Incidunnipsum dolore obcaecati tempore quibusdam reiciendis exercitationem debitis dignissimos molestiae animi",
          salary: 2094,
          age: "22 years",
          lastDate: "24 jun 2023",
        },
        {
          id: 2,
          title: "Need Web Developer",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit Incidunnipsum dolore obcaecati tempore quibusdam reiciendis exercitationem debitis dignissimos molestiae animi",
          salary: 2094,
          age: "22 years",
          lastDate: "24 jun 2023",
        },
        {
          id: 3,
          title: "Need Web Developer",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit Incidunnipsum dolore obcaecati tempore quibusdam reiciendis exercitationem debitis dignissimos molestiae animi",
          salary: 2094,
          age: "22 years",
          lastDate: "24 jun 2023",
        },
        {
          id: 4,
          title: "Need Web Developer",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit Incidunnipsum dolore obcaecati tempore quibusdam reiciendis exercitationem debitis dignissimos molestiae animi",
          salary: 2094,
          age: "22 years",
          lastDate: "24 jun 2023",
        },
      ],
    };
  },
};
</script>
