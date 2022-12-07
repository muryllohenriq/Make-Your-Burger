<template>
    <div id="burger-table">
        <div>
            <div id="burger-table-heading">
                <div class="order-id">#:</div>
                <div>Cliente:</div>
                <div>Pão:</div>
                <div>Carne:</div>
                <div>Opcionais:</div>
                <div>Ações:</div>
            </div>
        </div>
        <div id="burger-table-rows">
            <div class="burger-table-row" v-for="burger in burgers" :key="burger.id">
                <div class="order-number">1</div>
                <div>João</div>
                <div>Pão</div>
                <div>Maminha</div>
                <div>
                    <ul>
                        <li>Salame</li>
                        <li>Tomate</li>
                    </ul>
                </div>
                <div>
                    <select name="status" class="status">
                        <option value="">Selecione</option>
                    </select>
                    <button class="delete-btn">Cancelar</button>
                </div>
            </div>
            <div class="burger-table-row">
                <div class="order-number">1</div>
                <div>João</div>
                <div>Pão</div>
                <div>Maminha</div>
                <div>
                    <ul>
                        <li>Salame</li>
                        <li>Tomate</li>
                    </ul>
                </div>
                <div>
                    <select name="status" class="status">
                        <option value="">Selecione</option>
                    </select>
                    <button class="delete-btn">Cancelar</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dashboard",
    data() {
        return {
            burgers: null,
            burger_id: null,
            status: []
        }
    },
    methods: {
        // Função assíncrona
        async getPedidos() {
            // faz a requisição
            const req = await fetch("http://localhost:3000/burgers");
            // transforma a requisição em json
            const data = await req.json();
            // os dados que estão vindo estão sendo transformados em burgers, troca o valor de null pelo que veio do servidor
            this.burgers = data;
            // resgatar os status
        }
    },
    mounted() {
        // vai chamar o getPedidos
        this.getPedidos()
    }
}
</script>

<style scoped>
    #burger-table {
        max-width: 1200px;
        margin: 0 auto;
    }

    #burger-table-heading,
    #burger-table-rows,
    .burger-table-row{
        display: flex;
        flex-wrap: wrap;
    }

    #burger-table-heading {
        font-weight: bold;
        padding: 12px;
        border-bottom: 3px solid #333;
    }

    #burger-table-heading div,
    .burger-table-row div {
        width: 19%;
    }

    .burger-table-row {
        width: 100%;
        padding: 12px;
        border-bottom: 1px solid #CCC;
    }

    #burger-table-heading .order-id,
    .burger-table-row .order-number {
        width: 5%;
    }

    select {
        padding: 12px 6px;
        margin-right: 12px;
    }

    .delete-btn {
        background-color: #222;
        color: #FCBA03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .3s;
    }

    .delete-btn:hover {
        background-color: transparent;
        color: #222;
    }
</style>