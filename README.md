# shop365

https://www.figma.com/design/03N1kcCxpOtDmaa1KrHu2F/Shop365?node-id=0-1&t=XF4HqBv93BPEkkQx-0

https://replit.com/@nicholasmacedoo/trip-shop365#index.html

https://dummyjson.com/docs/products#products-all
docs > Products > Get all product> fecth

coloca no get do Postman
so obter os dados


async function getProdutoId(){
    const resposta =  await fetch('http:....')
    const data await resposta.json()
    console.log(data)
}
   
getProdutoId()

Inspecionar >rede > ultima linha > cabeçalho - verifica de onde veio (API)

docs > Products > Add product> fecth

async function addProduto(){
    const resposta =  await fetch('http:..../add' , {
        method: 'POST',
        body: JSON.stringify({})
            title: 'meu produto',
            price: 25,
   }), 
    headers: {  <!-- quais as consigurações-->
        'Content-Type: 'application/json'
    }
    const data await resposta.json()
    console.log(data)
}
   
addProduto()

docs > Products > Update product> fecth
PUT - conjunto de informações ou tudo
PATCH - uma informação específica

async function updateProduto(idProduto){
    const resposta =  await fetch('http:..../' + idProduto , {
        method: 'PUT', 
        body: JSON.stringify({})
            title: '2024',
            price: 0,50,
   }), 
    headers: {  <!-- quais as configurações-->
        'Content-Type: 'application/json'
    }
    const data await resposta.json()
    console.log(data)
}
   
updateProduto()


docs > Products > delete a product> fecth

async function deleteProduto(idProduto){
    const resposta =  await fetch('http:..../' + idProduto , {
        method: 'DELETE',
   }), 
    const data await resposta.json()
    console.log(data)
}
   
deleteProduto()