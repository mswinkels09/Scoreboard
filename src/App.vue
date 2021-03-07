<template>
  <div id="app">
    <MatchupTitle :team1="team1" :team2="team2"></MatchupTitle>
    <Scorecard :score="team1.score" @add-point="updateTeamScore(team1, 1)" @substract-point="updateTeamScore(team1, -1)"></Scorecard>
    <Scorecard :score="team2.score" @add-point="updateTeamScore(team2, 1)" @substract-point="updateTeamScore(team2, -1)"></Scorecard>
    <Gamestatus :team1="team1" :team2="team2"></Gamestatus>
  </div>
</template>

<script>
import MatchupTitle from "./components/MatchupTitle.vue";
import  Scorecard  from "./components/Scorecard";
import  Gamestatus  from "./components/Gamestatus";

export default {
  components: {MatchupTitle, Scorecard, Gamestatus},

  data () {
    return{
      team1: {
        name: "Team 1",
        score: 0
      },
      team2: {
        name: "Team 2",
        score: 0
      }
    }
  },

  methods: {
    updateTeamScore(team, points) {
      const updated= team.score + points;

      if (updated >= 0) {
        team.score = updated
      }
    }
  }
};
</script>

<style></style>
