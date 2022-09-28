<template>

    <div class="form-group d-flex justify-content-center">
        <img src="https://iguatemi.com.br/esplanada/sites/esplanada/files/logo-1360189941485.png" width="100px" alt="Fuzzy Cardigan"
    class="img-thumbnail img-responsive"  >
    </div>
    
    <div class="container ">
    
        <form action=""  method="GET" name="formulario" > 
    

            <div class="form-group">
                <div class="col-md-6 offset-md-3">
                    <label> Nome do produto ou sintoma </label>  
                    <input type="text" name="produtos" id="produtos" placeholder="Informe aqui o produto ou sintoma que está sentindo..." class="form-control" required>
                </div>
            </div>      
    
            <div class="form-group">
                <div class="col-md-6 offset-md-3" style="margin-bottom: 2rem;">
                    <input type="submit" value="buscar" class="btn btn-primary" name="" >
                </div>
            </div>
        </form> 
    </div>
</template>

<script>
    import api from '@/services/api.js'
    export default {
        // eslint-disable-next-line vue/multi-word-component-names
        name: 'Formulario',
        mounted() {
            api.get('http://127.0.0.1:8001/produtos/desodorante').then(response => {
                console.log(response.data)
            })
        }
    }
</script>