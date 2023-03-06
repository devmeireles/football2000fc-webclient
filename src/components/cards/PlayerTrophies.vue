<template>
    <div class="player-trophies">
        <p class="section-title">Titles and Victories</p>
        <div class="player-trophies__list">
            <div class="player-trophies__list-trophy" v-for="trophy in trophies" :key="trophy.name">
                <div class="player-trophies__list-trophy__image">
                    <img :src="trophy.image" :alt="trophy.name">
                </div>
                <div class="player-trophies__list-trophy__description">
                    <p>{{ trophy.name }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'player-trophies',
    data() {
        return {
            trophies: [
                {
                    name: 'Champions League',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/4.png?lm=1520606999'
                },
                {
                    name: 'FIFA Club World Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/318.png?lm=1520606999',
                },
                {
                    name: 'German',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/10.png?lm=1520606996',
                },
                {
                    name: 'Spanish Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/11.png?lm=1520606997',
                },
                {
                    name: 'UEFA Super Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/354.png?lm=1520606999',
                },
                {
                    name: 'German Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/27.png?lm=1520606999',
                },
                {
                    name: 'German Super Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/312.png?lm=1520606999',
                },
                {
                    name: 'Spanish Super Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/93.png?lm=1520606999',
                },
                {
                    name: 'Footballer of the Year',
                    image: 'https://tmssl.akamaized.net/images/titel/medium/4.png?lm=1465908580',
                },
                {
                    name: 'UEFA Nations League',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/601.png?lm=1653914395',
                },
                {
                    name: 'Copa América',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/106.png?lm=1461847499',
                },
                {
                    name: 'English Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/47.png?lm=1520606999',
                },
                {
                    name: 'Copa Sudamericana',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/154.png?lm=1520606999',
                },
                {
                    name: 'Under-20 World Cup',
                    image: 'https://tmssl.akamaized.net/images/erfolge/medium/160.png?lm=1461847499',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.player-trophies {
    display: flex;
    flex-direction: column;

    &__list {
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: center;
        margin-top: 15px;

        &-trophy {
            padding: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 20%;

            &__description {
                width: 75%;

                p {

                    text-align: center;
                    font-size: 13px;
                    font-weight: 700;
                }
            }
        }
    }
}
</style>