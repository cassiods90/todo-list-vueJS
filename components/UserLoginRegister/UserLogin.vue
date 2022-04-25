<template>
	<div class="login-register login-content d-flex flex-column justify-content-center align-items-center">
		<span class="text subtitle base-color">Execute Login</span>
		<div class="login-links d-flex flex-column justify-content-center align-items-center">
			<FormulateForm>
				<div class="form-row">
					<div class="form-group col-12">
						<div class="field-input-wrapper">
							<label class="text black">Email</label>
							<FormulateInput
								type="text"
								validation="required"
								placeholder="Enter your e-mail"
								:wrapper-class="['field-input']"
							/>
						</div>
					</div>

					<div class="form-group col-12">
						<div class="field-input-wrapper">
							<label class="text black">Password</label>
							<FormulateInput
								type="text"
								validation="required"
								placeholder="Enter your password"
								:wrapper-class="['field-input']"
							/>
						</div>
					</div>   

					<div class="form-group col-12">
						<div class="field-input-wrapper">
							<FormulateInput
							type="submit"
							name="Login"
							:wrapper-class="['field-button-formulate']"
							/>
						</div>
					</div>   		
				</div>
			</FormulateForm>
		</div>	
	</div>
</template>


<script>
	export default {
		name: 'UserLogin',
		data() {
			return {
				
			};
		},
		methods: {
			
		},
		components: {
			
		}
	};
</script>