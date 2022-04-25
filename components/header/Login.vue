<template>
    <div>
        <div class="login-register d-flex">

            <nuxtLink class="login-register-item d-flex justify-content-center align-items-center" to="/panel" v-if="isLogged">
                <svgIconPanel/> 
                <span class="text headertext uppercase white">My Panel</span>     
            </nuxtLink>

            <nuxtLink class="login-register-item d-flex justify-content-center align-items-center" to="/loginRegister" v-else >
                <svgIconLogin/>               
                <span class="text headertext uppercase white">Login / Create Account</span>   
            </nuxtLink>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Login',
    data() {
			return {
				isLogged: false,
			};
		},
}
</script>