<template>
    <div class="user-infos-form">
        <div class="row justify-content-center">
            <div class="col-12" data-aos="fade-up" data-aos-delay="200">
                <FormulateForm>
                    <div class="form-row">
                        <div class="form-group col-12 col-md-6">
                            <div class="field-input-wrapper">
                                <label class="text black">User</label>
                                <FormulateInput
                                    type="text"
                                    validation="required"
                                    :wrapper-class="['field-input']"
                                />
                            </div>
                        </div>

                        <div class="form-group col-12 col-md-6">
                            <div class="field-input-wrapper">
                                <label class="text black">Password</label>
                                <FormulateInput
                                    type="text"
                                    validation="required"
                                    :wrapper-class="['field-input']"
                                />
                            </div>
                        </div>

                        <div class="form-group col-12 col-md-6">
                            <div class="field-input-wrapper">
                                <label class="text black">Name</label>
                                <FormulateInput
                                    type="text"
                                    validation="required"
                                    :wrapper-class="['field-input']"
                                />
                            </div>
                        </div>

                        <div class="form-group col-12 col-md-6">
                            <div class="field-input-wrapper">
                                <label class="text black">Email</label>
                                <FormulateInput
                                    type="text"
                                    validation="required"
                                    :wrapper-class="['field-input']"
                                />
                            </div>
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
                    
                </FormulateForm>
            </div>
        </div> 
    </div>
</template>

<script>
export default {
    name: 'PanelUserInfos',
    data() {
			return {
				
			};
		},
}
</script>