<template>
    <div class="detailed-player-stats">
        <p class="section-title">Stats</p>
        <div class="detailed-player-stats__body">
            <table class="table" cellspacing="0" cellpadding="0">
                <thead>
                    <tr>
                        <th>Seasson</th>
                        <th style="width:60px;">League</th>
                        <th style="width:60px;">Club</th>
                        <th>Squad</th>
                        <th>Apps</th>
                        <th>Goals</th>
                        <th>Assists</th>
                        <th>Own Goals</th>
                        <th>Subs On</th>
                        <th>Subs Off</th>
                        <th>Yellow Card</th>
                        <th>2nd Yellow Card</th>
                        <th>Red Card</th>
                        <th>Penalty Goals</th>
                        <th>Minutes per Goal</th>
                        <th>Minutes Played</th>
                    </tr>
                </thead>

                <tbody>
                    <tr v-for="item in stats">
                        <td>{{ item.season }}</td>
                        <td style="width:100px;">
                            <img class="league" :src="item.leagueFlag" :alt="item.league" />
                        </td>
                        <td><img class="club" :src="item.clubFlag" :alt="item.club" /></td>
                        <td>{{ item.squad }}</td>
                        <td>{{ item.apps }}</td>
                        <td>{{ item.goals }}</td>
                        <td>{{ item.assists }}</td>
                        <td>{{ item.ownGoals }}</td>
                        <td>{{ item.subsOn }}</td>
                        <td>{{ item.subsOff }}</td>
                        <td>{{ item.yellowCard }}</td>
                        <td>{{ item.secondYellowCard }}</td>
                        <td>{{ item.redCard }}</td>
                        <td>{{ item.penaltyGoals }}</td>
                        <td>{{ item.minutesPerGoal }}</td>
                        <td>{{ item.minutesPlayed }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: 'detailed-player-stats',
    data() {
        return {
            stats: [
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                },
                {
                    id: 1,
                    season: 2022,
                    club: 'Rayo Vallecano',
                    clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
                    league: 'La Liga',
                    leagueFlag: 'https://assets.laliga.com/assets/logos/laliga-h/laliga-h-600x600.png',
                    squad: 10,
                    apps: 9,
                    goals: 2,
                    assists: 4,
                    ownGoals: 0,
                    subsOn: 0,
                    subsOff: 2,
                    yellowCard: 1,
                    secondYellowCard: 0,
                    redCard: 2,
                    penaltyGoals: 1,
                    minutesPerGoal: 120,
                    minutesPlayed: 1200,
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.detailed-player-stats {
    .table {
        width: 100%;

        thead {
            height: 30px;

            th {

                font-weight: 700;
            }
        }

        tbody {
            tr {
                border: none;
                height: 40px;

                &:nth-child(even) {
                    background-color: #f2f2f2;
                }

                td {
                    text-align: center;
                    outline: 1px solid #b4b4b4;

                    img.league {
                        width: 50px;
                    }

                    img.club {
                        width: 30px;
                    }
                }
            }


        }
    }
}
</style>