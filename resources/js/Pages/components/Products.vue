<template>
    <div class="products" id="products">
        <div class="products__content">
            <div class="products__content__left">
                <div class="products__content__left__text">
                    <p class="products__content__left__text__title">À PROPOS</p>
                    <p class="products__content__left__text__about">AGENCE DE COMMUNICATION DIGITALE</p>
                    <p class="products__content__left__text__extra">Notre mission est d’imaginer un univers graphique en mouvement qui raconte une histoire unique : celle de votre projet.</p>
                </div>

                <div class="products__content__left__products">
                    <ProductCard :title="'MOTION DESIGN'" :extra="'Nous réalisons vos vidéos explicatives et vos publicités pour présenter vos services de la meilleure façon possible.'"/>
                    <ProductCard :title="'SITE WEB / APPLICATIONS'" :extra="'Nous développons des sites web / applications sur mesure qui correspondent à tous vos besoins.'" />
                    <ProductCard :title="'CORPORATE BRANDING'" :extra="'Logo, charte graphique, flyers... Nous accompagnons les entreprises dans la définition de leur identité.'" />
                </div>
            </div>

            <div class="products__content__right">
                <img src="../assets/personOnComputer.svg" alt="Person On Computer" class="products__content__right__img">
            </div>
        </div>

        <div class="products__skewy"></div>
    </div>
</template>

<script>
import ProductCard from './ProductCard.vue';
export default {
    Name: "Products",
    components: {
        ProductCard
    }
}
</script>

<style lang="scss">
.products {
    background-color: var(--color-blue);

    width: 100%;
    height: 60rem;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

    &__content {
        display: flex;
        height: 50rem;
        width: 90rem;

        margin-top: 3rem;

        &__left {
            width: 50%;
            height: 100%;

            display: flex;
            flex-direction: column;
            align-items: center;

            border-left: 1px solid white;

            &__products {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;

                width: 35rem;
                height: 30rem;

                margin-top: 3rem;
            }

            &__text {
                width: 35rem;
                height: 16rem;

                display: flex;
                flex-direction: column;
                justify-content: space-between;

                &__title {
                    color: var(--color-yellowGreen);
                    font-size: 1.4rem;
                    font-weight: 600;
                }

                &__about {
                    color: white;
                    font-size: 2.5rem;
                    font-weight: 600;
                }

                &__extra {
                    font-size: 1.3rem;
                    color: rgb(199, 199, 199);
                    font-weight: 600;
                }
            }
        }

        &__right {
            width: 50%;
            height: 100%;

            display: flex;
            justify-content: center;
            align-items: center;

            &__img {
                aspect-ratio: 969/1300;

                height: 90%;
            }
        }
    }
}

@media screen and (max-width: 1200px) {
    .products {
        &__content {
            width: 80rem;
        }
    }
}

@media screen and (max-width: 1100px) {
    .products {
        &__content {
            width: 65rem;

            &__left {
                &__products {
                    width: 25rem;
                }

                &__text {
                    width: 25rem;

                    &__about {
                        font-size: 2.2rem;
                    }

                    &__extra {
                        font-size: 1.1rem;
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 800px) {
    .products {
        &__content {
            justify-content: center;

            width: 50rem;

            &__left {
                width: 100%;

                &__products {
                    width: 40rem;
                }

                &__text {
                    width: 40rem;

                    &__about {
                        font-size: 2.6rem;
                    }

                    &__extra {
                        font-size: 1.2rem;
                    }
                }
            }

            &__right {
                display: none;
                width: 0%;
                height: 0%;
            }
        }
    }
}

@media screen and (max-width: 650px) {
    .products {
        &__content {
            width: 40rem;

            &__left {
                &__products {
                    width: 30rem;
                }

                &__text {
                    width: 30rem;

                    &__about {
                        font-size: 2.4rem;
                    }

                    &__extra {
                        font-size: 1.2rem;
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 500px) {
    .products {
        &__content {
            width: 27rem;

            &__left {
                &__products {
                    width: 23rem;
                }

                &__text {
                    width: 23rem;

                    &__about {
                        font-size: 2.2rem;
                    }

                    &__extra {
                        font-size: 1.1rem;
                    }
                }
            }
        }
    }
}
</style>