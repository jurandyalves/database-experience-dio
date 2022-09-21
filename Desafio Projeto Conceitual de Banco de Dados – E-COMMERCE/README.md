# Desafio Projeto Conceitual de Banco de Dados – E-COMMERCE
Conforme descrito no desafio o objetivo era refinar o modelo apresentado acrescentando os seguintes pontos:

Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
-> Para solucionar este ponto coloquei o campo identificação(CPF/CNPJ) e email como Unique, para que não se pudesse fazer dois cadastro com o mesmo CPF/CNPJ e mesmo endereço de e-mail.

Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
-> Para solucionar este ponto, como um pedido pode ter a possibilidade de ser pago com mais de uma forma de pagamento e uma forma de pagamento pode pagar mais de um pedido, criei uma nova entidade(forma_pagamento) e uma entidade (relacao_pedido_forma_de_pagamento) para salvar a relação entre pedido e forma de pagamento.

Entrega – Possui status e código de rastreio;
-> Criei uma nova entidade (entrega) com os dados de código de rastreio e status relacionada ao pedido com um relacionamento de 1:n pois um pedido só pode haver de ter mais de um código de rastreio vinculado devido à possibilidade de os produtos do pedido serem de vendedores diferentes e estarem em diferentes localidades, ocasionando assim a necessidade de emissão de mais de um código de rastreio/entrega para acompanhamento da entrega dos produtos daquele pedido.
