
<script>
    export default {
        name: 'Calculadora',
        data() {
            return {
                num1: 0,
                num2: 0,
                operacao: '+'
            }
    },
        computed: {
            resultado() {
                switch (this.operacao) {
                    case '+': return this.num1 + this.num2
                    case '-': return this.num1 - this.num2
                    case '*': return this.num1 * this.num2
                    case '/':
                        return this.num2 !== 0 ? (this.num1 / this.num2).toFixed(2) : 'Erro: divisão por zero'
                    default: return ''
                }
            }
        }
    }
</script>

<template>
    <div class="calculadora">
        <input type="number" v-model.number="num1" placeholder="Número 1" />
        <input type="number" v-model.number="num2" placeholder="Número 2" />

        <select v-model="operacao">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>

        <p><strong>Resultado:</strong> {{ resultado }}</p>
    </div>
</template>

<style scoped>
    .calculadora {
        display: flex;
        flex-direction: column;
        gap: 10px;
        max-width: 300px;
        margin: 0 auto;
    }
</style>
