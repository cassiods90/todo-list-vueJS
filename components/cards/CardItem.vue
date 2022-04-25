
<template>
    <a href="javascript:void(0)" class="professional-card-item d-flex flex-column justify-content-start align-items-start" @click="toggleCartModal">
        <div class="card-item-image">
            <img :src="value.professionalPicture" alt="">
        </div>
        <div href="javascript:void(0)" class="card-item-content d-flex flex-column justify-content-center">
            <span class="text subtitle base-color item-title">{{value.professionalName}}</span>
            <span class="text black">{{value.professionalSpeciality}}</span>
            <span class="text black">{{value.professionalAddress}}</span>
            <span class="text black">{{value.professionalPhone}}</span>
            <span class="text base-color item-info">+ More Info</span>
        </div>
        <CardItemModal :showCartModal="showCartModal" @toggleCartModal="toggleCartModal" :value="value"/>
    </a>

    
</template>

<script>
import CardItemModal from '@/components/cards/CardItemModal';

export default {
    name: 'CardItem',
    components: {
        CardItemModal,
    },
    props: {
        value: {
        type: Object,
        required: true,
        },
    },
    data: function () {
        return {
            showCartModal: false,
        }
    },
    watch: {
        
    },
    methods: {
        toggleCartModal() {
            this.showCartModal = !this.showCartModal;
        },
        closeCartModal() {
            this.showCartModal = !this.showCartModal;
            console.log('click close')
        },
    },
}
</script>