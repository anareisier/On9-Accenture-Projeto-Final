FALTOU

Revisar variáveis e msg de erro
EDITAR DESCRITIVO
DEIXAR TUDO EM PORTUGUÊS
TESTAR TODAS AS ROTAS
!!!!!!!PREPARAR APRESENTAÇÃO!!!!!!

## Faltou

  - Validação
  - deixar tudo em inglês
  - demais funcionalidades

## Validação que não deu certo

vendedor
const yup = require("yup")

exports.vendedorSchema = yup.object().shape({
    nome: yup.string().required('Esse campo é obrigatório'),
    rg: yup.number().required('Esse campo é obrigatório'),
    passoword: yup.string().required('Esse campo é obrigatório')
  }).required('O formulário não pode ser vazio')

estoque
const yup = require("yup")


const produtoSchema = yup.object().shape({
    nomeProduto: yup.string().required('O nome do produto é obrigatório'),
    descricao: yup.string().required('A descrição é obrigatório'),
    estoque: yup.number().required('O campo estoque é obrigatório'),
    valorFabrica: yup.number().required('Esse campo é obrigatório')
  }).required('O formulário não pode ser vazio')


  const estoqueSchema = yup.object().shape({
    nomeProduto: yup.string().required('O nome do produto é obrigatório'),
    estoque: yup.number().required('O campo estoque é obrigatório'),
  }).required('O formulário não pode ser vazio')

  yup.setLocale({
    string:{
      nomeProduto: "Dado inserido incorretamente",
      descricao: "Dado inserido incorretamente",
      estoque: "Dado inserido incorretamente",
      valorFabrica: "Dado inserido incorretamente",
    },   
})

module.exports ={
  produtoSchema,
  estoqueSchema
}


vendas

const yup = require("yup")

const vendaSchema = yup.object().shape({
    nomeProduto: yup.string().required('Esse campo é obrigatório'),
    valorVenda: yup.number().required('Esse campo é obrigatório'),
    quantidade: yup.number().required('Esse campo é obrigatório'),
    vendedor: yup.string().required('Esse campo é obrigatório'),
    clienteContato: yup.array().required('Esse campo é obrigatório')
  }).required('O formulário não pode ser vazio')

module.exports = vendaSchema