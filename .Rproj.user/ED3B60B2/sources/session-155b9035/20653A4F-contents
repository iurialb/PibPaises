library(tidyverse)
read_csv("(2) pib_paises.csv")
pib_paises <- read_csv("(2) pib_paises.csv")

# A base possui valores desnecessários e fora do padrão nas últimas linhas. Além disso, possui alguns valores vazios. O primeiro passou será excluir essas informações.
# Nesse sentido, o código abaixo demonstra a subtração das linhas 267 até a 271, que contem essas informações.
# E das colunas 2 e 4, que contém o valor duplicado do ano e o código dos países (informação desnecessária visto que já temos os países).

pib_paises_2 <- pib_paises[-c(267:271), -c(2,4)]

# Considerando que os títulos das colunas estão impraticáveis, se faz necessário a criação de um vetor pra modança dos nome que facilite o entendimento:

nomes <- c("ano","paises_regioes","var_pib_capita","var_pib_total")
names(pib_paises_2) <- nomes

# Outro fator que está poluindo o banco de dados é o fato de todas as variáveis estarem identificadas como caracteres
# Pra isso é necessário criar novas variáveis contendo valores com a expressão as.numeric

pib_paises_2$var_pib_capita_ajust <- as.numeric(pib_paises_2$var_pib_capita)
pib_paises_2$var_pib_total_ajust <- as.numeric(pib_paises_2$var_pib_total)

#Por fim, podemos criar algumas estatísticas descritivas das duas variáveis novas

summary(pib_paises_2$var_pib_capita_ajust)
summary(pib_paises_2$var_pib_total_ajust)

