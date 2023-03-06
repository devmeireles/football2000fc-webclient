<template>
    <div class="profile-card">
        <div class="profile-card__profile">
            <div class="profile-card__profile-image">
                <img :src=profileImage :alt=name>
            </div>

            <div class="profile-card__title">
                <h1 class="card-title">{{ formatedName }}</h1>
            </div>

            <div class="profile-card__profile-stats">
                <div class="profile-card__profile-stats__stat">
                    <p><strong>Position:</strong> {{ position }}</p>
                </div>

                <div class="profile-card__profile-stats__stat">
                    <p><strong>Place of Birth:</strong> {{ placeBirth }}</p>
                </div>

                <div class="profile-card__profile-stats__stat">
                    <p><strong>Age:</strong> {{ age }}</p>
                </div>

                <div class="profile-card__profile-stats__stat">
                    <p><strong>Height:</strong> {{ height }}</p>
                </div>

                <div class="profile-card__profile-stats__stat">
                    <p><strong>National Team:</strong> {{ nationalTeam }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'player-card',
    data() {
        return {
            name: "Gabriel Meireles",
            number: 10,
            profileImage: 'http://placekitten.com/120/150',
            position: 'Developer',
            age: '09/12/1993 - 29',
            height: '1,92',
            placeBirth: 'São Paulo - Brazil',
            nationalTeam: '99 Games, 70 Goals, 10 Assists'
        }
    },
    computed: {
        formatedName() {
            let res;

            if (this.number) res = `#${this.number} `;
            if (this.name) res += this.name;
            return res;
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/mixins';
@import '@/assets/variables';

.profile-card {
    display: flex;
    flex-direction: column;

    &__title {
        display: none;

        @include for-phone-only {
            display: block;
        }
    }

    &__profile {
        display: flex;
        flex-direction: row;
        align-items: flex-start;

        @include for-phone-only {
            flex-direction: column;
            align-items: center;
        }

        &-stats {
            padding-left: 15px;

            @include for-phone-only {
                padding: 0;
            }

            &__stat {
                p {
                    font-size: $body-font;

                    strong {
                        font-weight: bold;
                    }
                }
            }
        }
    }
}
</style>