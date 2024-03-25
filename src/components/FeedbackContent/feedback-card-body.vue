<template>
    <div>
        <VRow>
            <VCol>
                <h1 style="color: #0F172A;"><b>Because they love us</b></h1>
            </VCol>
            <VCol style="float: right;"> <!-- Önceki ve sonraki butonlar -->
                <VBtn variant="outlined" v-if="currentIndex > 0" @click="prevSlide" icon="mdi-chevron-left"
                    style="margin: 5px;" />
                <VBtn variant="outlined" v-if="currentIndex * 6 < items.length" @click="nextSlide" style="margin: 5px;"
                    icon="mdi-chevron-right" />
            </VCol>
        </VRow>
        <VRow v-if="isScreenSmall">
            <VCarousel :show-arrows="false" v-model="currentIndex" cycle hide-delimiters hide-controls controls="true">
                <VCarousel-item v-for="(item, index) in items" :key="index">
                    <VRow justify="center" align="center">
                        <VCol cols="12" sm="4" v-for="(item, index) in getItems(index)" :key="index">

                        </VCol>
                    </VRow>
                    <VCard class="pa-3" style="background-color:white; width: 100%; height: 50%;">
                        <div>
                            <VRow>
                                <VCol>
                                    <VImg :src="item.fLogo" max-width="300" height="20px" />

                                </VCol>
                                <VCol>
                                    <p>{{ item.title }}</p>
                                </VCol>
                            </VRow>
                        </div>
                        <p>{{ item.content }}</p>
                        <VRow>
                            <VAvatar color="primary" variant="tonal">
                                <VImg :src="item.image" :alt="item.name" />
                            </VAvatar>
                            <div class="flex-grow-1 ms-4 overflow-hidden">
                                <h6 class="text-base font-weight-regular">
                                    {{ item.name }}
                                </h6>
                                <span class="d-block text-sm text-truncate text-disabled">{{ item.rank }}</span>
                            </div>

                        </VRow>
                    </VCard>
                </VCarousel-item>
            </VCarousel>
        </VRow>
        <VRow v-else style="background-color: #F2D888; width: 100%; height: 200px;">
            <VCarousel :show-arrows="false" v-model="currentIndex" cycle hide-delimiters hide-controls controls="true">
                <VCarousel-item v-for="(item, index) in items" :key="index">
                    <VRow justify="center" align="center">
                        <VCol cols="12" sm="4" v-for="(item, index) in getItems(index)" :key="index">
                            <VCard class="pa-3" style="background-color:white; width: 100%; height: 50%;">
                                <div>
                                    <VRow>
                                        <VCol>
                                            <VImg :src="item.fLogo" class="mx-auto" max-width="300" height="20px" />
                                        </VCol>
                                        <VCol><span>{{ item.title }}</span></VCol>
                                    </VRow>
                                </div>
                                <p>{{ item.content }}</p>
                                <VRow>
                                    <VAvatar color="primary" variant="tonal">
                                        <VImg :src="item.image" :alt="item.name" />
                                    </VAvatar>
                                    <div class="flex-grow-1 ms-4 overflow-hidden">
                                        <h6 class="text-base font-weight-regular">
                                            {{ item.name }}
                                        </h6>
                                        <span class="d-block text-sm text-truncate text-disabled">{{ item.rank }}</span>
                                    </div>

                                </VRow>
                            </VCard>
                        </VCol>
                    </VRow>
                </VCarousel-item>
            </VCarousel>
        </VRow>
    </div>
</template>

<script>
import avatar1 from "../../assets/images/avatars/avatar-1.png";
import avatar2 from "../../assets/images/avatars/avatar-2.png";
import avatar3 from "../../assets/images/avatars/avatar-3.png";
import avatar4 from "../../assets/images/avatars/avatar-4.png";
import avatar5 from "../../assets/images/avatars/avatar-5.png";
import flogo1 from "../../assets/images/feedback/fLogo1.png";
import flogo2 from "../../assets/images/feedback/fLogo2.png";
import flogo3 from "../../assets/images/feedback/fLogo3.png";
import flogo4 from "../../assets/images/feedback/fLogo4.png";
export default {
    data() {
        return {
            currentIndex: 0,
            items: [
                { title: 'Zoomer', fLogo: flogo1, content: 'Lorem ipsum dolor sit amet,  incididunt ut labore et dolore magna aliqua.', image: avatar1, name: "Hellen Jummy", rank: "Office Manager" },
                { title: 'Shell', fLogo: flogo2, content: 'now use Lorem Ipsum as their default model text, and a search for lorem ipsum will uncover', image: avatar2, name: "David Oshodi", rank: "Software Developer" },
                { title: 'Artvenue', fLogo: flogo3, content: 'There are many variations of passages of Lorem Ipsum available, but the majority have suffered ', image: avatar3, name: "Hellena John", rank: "Co-founder" },
                { title: 'Walker', fLogo: flogo4, content: 'onsectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical', image: avatar4, name: "Alex Jummy", rank: "Frontend Developer" },
                { title: 'Tryend', fLogo: flogo1, content: 'This book is a treatise on the theory of ethics, very popular during the Renaissance.', image: avatar5, name: "Olivia Dacel", rank: "Team Lead" },
                { title: 'Shell', fLogo: flogo4, content: 'now use Lorem Ipsum as their default model text, and a search for lorem ipsum will uncover', image: avatar2, name: "Brice Jummy", rank: "Backend Developer" },
                // Diğer kartlar buraya eklenebilir
            ],
            isScreenSmall: false
        };
    },
    methods: {
        prevSlide() {
            this.currentIndex--;
        },
        nextSlide() {
            this.currentIndex++;
        },
        getItems(index) {
            const start = index * 3;
            const end = start + 3;
            return this.items.slice(start, end);
        },
        handleResize() {
            this.isScreenSmall = window.innerWidth < 768; // Örnek bir eşik değeri, istediğiniz değeri kullanabilirsiniz
        }
    },
    created() {
        window.addEventListener('resize', this.handleResize);
        // Sayfa yüklendiğinde boyut kontrolü yapmak için
        this.handleResize();
    },
    destroyed() {
        window.removeEventListener('resize', this.handleResize);
    }
};
</script>

<style scoped>
.prev-btn,
.next-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 999;
}

.prev-btn {
    left: 0;
}

.next-btn {
    right: 0;
}

.element.style {
    height: 50%;
}
</style>