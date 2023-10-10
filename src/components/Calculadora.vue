<script setup>
import { ref, computed } from 'vue';

const numero1 = ref(0);
const numero2 = ref(0);
const operacao = ref('');

const resultado = computed(() => {
    switch (operacao.value) {
        case 'somar':
            return numero1.value + numero2.value;
        case 'diminuir':
            return numero1.value - numero2.value;
        case 'multiplicar':
            return numero1.value * numero2.value;
        case 'dividir':
            return numero1.value / numero2.value;
        default:
            return 0;
    }
})
</script>