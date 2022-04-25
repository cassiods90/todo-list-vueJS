<template>
	<div class="login-register register-content d-flex flex-column justify-content-center align-items-center">
				<span class="text subtitle base-color">Register new account</span>
				<div class="register-links d-flex flex-column justify-content-center align-items-center">
					<FormulateForm>
						<div class="register-form patient-form d-flex flex-wrap visible" id="patientForm">
							<div class="form-group col-12 col-lg-6">
								<div class="field-input-wrapper">
									<label class="text black">User</label>
									<FormulateInput
										type="text"
										validation="required"
										placeholder="Enter your user"
										:wrapper-class="['field-input']"
									/>
								</div>
							</div> 

							<div class="form-group col-12 col-lg-6">
								<div class="field-input-wrapper">
									<label class="text black">Email</label>
									<FormulateInput
										type="email"
										name="sample"
										placeholder="Your email"
										validation="required|email"
										:wrapper-class="['field-input']"
									/>
								</div>
							</div>

							<div class="form-group col-12 col-lg-6">
								<div class="field-input-wrapper">
									<label class="text black">Password</label>
									<FormulateInput
										type="password"
										name="password"
										placeholder="Enter your password"
										validation="required|min:08,length"
										:wrapper-class="['field-input']"
									/>
								</div>
							</div>

							<div class="form-group col-12 col-lg-6">
								<div class="field-input-wrapper">		
									<label class="text black">Confirm Password</label>
									<FormulateInput
										type="password"
										name="password_confirm"
										placeholder="Confirm your password"
										validation="required|confirm"
										validation-name="Password confirmation"
										:wrapper-class="['field-input']"
									/>
								</div>
							</div>  

							<div class="form-group col-12 col-lg-12">
								<div class="field-input-wrapper">
									<label class="text black">Name</label>
									<FormulateInput
										type="text"
										validation="required"
										placeholder="Enter your name"
										:wrapper-class="['field-input']"
									/>
								</div>
							</div> 

							<div class="form-group col-12">
								<div class="field-input-wrapper">
									<FormulateInput
									type="submit"
									name="Save"
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
		name: 'UserRegister',
		data() {
			return {
				
			};
		},
		methods: {
			
		},
	};
</script>