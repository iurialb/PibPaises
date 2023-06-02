library(tidyverse)
read_csv("(2) pib_paises.csv")
pib_paises <- read_csv("(2) pib_paises.csv")

# A base possui valores desnecessários e fora do padrão nas últimas linhas. Além disso, possui alguns valores vazios. O primeiro passou será excluir essas informações.
# Nesse sentido, o código abaixo demonstra a subtração das linhas 267 até a 271, que contem essas informações.
# E das colunas 2 e 4, que contém o valor duplicado do ano e o código dos países (informação desnecessária visto que já temos os países).

pib_paises_2 <- pib_paises[-c(267:271), -c(2,4)]
