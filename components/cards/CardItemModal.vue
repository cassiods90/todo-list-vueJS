
<template>
    <div class="professional-card-item-modal" :class="{open : showCartModal}">
        <div class="professional-card-item-modal-inner d-flex flex-column flex-lg-row justify-content-start align-items-start">
            <div class="card-item-image">
                <img :src="value.professionalPicture" alt="">
            </div>
            <a class="card-item-content d-flex flex-column justify-content-between align-items-center">
                <div class="div-top">
                    <span class="text title base-color item-title">{{value.professionalName}}</span>
                </div>

                <div class="div-middle d-flex flex-column justify-content-center align-items-start">
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Speciality:</span>
                        <span class="text black">{{value.professionalSpeciality}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Registry Number:</span>
                        <span class="text black">{{value.professionalRegister}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">E-mail:</span>
                        <span class="text black">{{value.professionalEmail}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Phone:</span>
                        <span class="text black">{{value.professionalPhone}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Whatsapp:</span>
                        <span class="text black">{{value.professionalWhatsapp}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Address:</span>
                        <span class="text black">{{value.professionalAddress}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Consult Value:</span>
                        <span class="text black">R$ {{value.professionalValue}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Opening Hours:</span>
                        <span class="text black">{{value.professionalOpeningHours}}</span>
                    </div>
                    <div class="d-flex justify-content-start align-items-center">
                        <span class="text subtitle black">Open Days:</span>
                        <span class="text black">{{value.professionalDays}}</span>
                    </div>
                </div>

                <div class="div-bottom">
                    <a href="https://www.google.com.br" class="text base-color item-info">+ Click here to schedule your time</a>
                </div>   
            </a>
            <a href="javascript:void(0)" class="modal-close" @click="closeCartModal">
                <img src="@/assets/images/global/close.png" alt=""> 
            </a>
        </div>
    </div>
</template>

<script>


export default {
    name: 'CardItemModal',
    props: {
        showCartModal:{
            required: true,
        },
        value: {
        type: Object,
        required: true,
        },
        
    },
    methods: {
        toggleCartModal() {
            this.$emit("showCartModal")
        },  
        closeCartModal() {
            this.$emit("closeCartModal")
        },       
    },
}
</script>