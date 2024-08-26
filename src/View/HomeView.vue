<script setup>
import { ref } from 'vue'
import DataTable from 'primevue/datatable';
import Column from 'primevue/column';

const formData = ref({
  username: '',
  password: '',
  confirmPassword: '',
  isAustralian: false,
  reason: '',
  gender: '',
  suburb: 'Clayton',
});

const submittedCards = ref([]);

const submitForm = () => {
    ValidateName(true)
    validatePassword(true)
    if (!errorMessages.value.username &&!errorMessages.value.password) {
        submittedCards.value.push({formData.value});
        clearForm();


</script>