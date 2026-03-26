

Não fiz ele pensando que alguem iria ler, por isso está com pouquissimos comentarios e de certa forma, desorganizado
mas a maior parte da desorganização que eu estou vendo aqui, é causada pelo GitHub
# O Codigo atual:

Algoritmo "PDE-O"
// Disciplina   : [Linguagem e Lógica de Programação]
// Professor   : Ricardo
// Descrição   : O Programa Faz uma serie de Exercicios com historia
// Autor(a)    : Jesus/Danilo
// Data atual  : 25/03/2026
Var
   protocolo, numeroProced, i, decidaExtra: inteiro
   nucleos, num1, num2: real
   enter: caractere
   
//=======================================
procedimento Separador
inicio
   escreval("[]----====----====----====----====----====----====----====----[]")
fimprocedimento

procedimento Enter
inicio
   escreval("Aperte [Enter] para continuar.")
   leia(enter)
      se (enter <> "") entao
         escreval("Eu disse para apertar [Enter]!!")
         timer 500
         timer 50
         Enter
      fimse
fimprocedimento

procedimento DigiteDoisNumeros
inicio
       escreval("Digite o primeiro número.")
       leia(num1)
       escreval("Digite o segundo número.")
       leia(num2)
fimprocedimento
//=========================
procedimento ExercicioUm
inicio
   Separador
   timer 500
   escreval("inicializando sistema...")
   escreval("Pré-aquecendo núcleos...")
   timer 500
   timer 50
   escreval("")
   
   para i de 0 ate 10 passo 1 faca
      timer 35*i
      escreval("Núcleos pré-aquecidos: ", i,"...")
   fimpara
   timer 50
   Separador
   escreval("Todos os núcleos foram pré-aquecidos.")

   escreval("")
   timer 1500
   escreval("Iniciando a próxima etapa...")
   timer 2000
   timer 50
   limpatela
fimprocedimento
//=========================
procedimento ExercicioDois
inicio

   Separador
   escreval("Digite os Protocolos e Sistemas a serem utilizados.")
   escreval("Lembre-se, eles só existem em numeros inteiros.")
   escreval("Digite [0] para executar a coletânea de Protocolos e Sistemas.")

   repita
      numeroProced <- numeroProced + protocolo
      leia(protocolo)

   ate (protocolo = 0)
   Separador
   escreval("O número de procedimentos que deverão ser feitos são", numeroProced, ".")

   escreval("")
   timer 1500
   escreval("Iniciando a próxima etapa...")
   timer 2000
   timer 50
   limpatela
fimprocedimento
//=========================
procedimento ExercicioTres
inicio

   Separador
   escreval("Digite o número de núcleos a serem usados para ")
   escreval("executar", numeroProced," procedimentos.")
   escreval("Temos 10 núcleos e podemos usar um núcleo parcialmente")

   repita
      leia(nucleos)
   se (nucleos > 0) e (nucleos <= 10) entao
   senao
      escreval("Não temos essa quantidade de núcleos")
   fimse
   ate (nucleos > 0) e (nucleos <= 10)

   Separador
   escreval("O número de núcleos que serão utilizados são:", nucleos)

   escreval("")
   timer 1500
   escreval("Iniciando a próxima etapa...")
   timer 2000
   timer 50
   limpatela
fimprocedimento
//=========================
procedimento ExercicioQuatro
inicio

   Separador
   escreval("Digite o protocolo a ser verificado.")
   leia(protocolo)
   escreval("Calculando a quantidade de micro-erros a serem cometidos segundo")
   escreval(" a quantidade de protocolos interagindo com o protocolo Nº", protocolo)
   timer 5000
   timer 50
   Separador

   para i de 1 ate 10 passo 1 faca
      timer 10*i
      escreval("Se há [", i, "] protocolos interagindo com o protocolo Nº", protocolo)
      escreval("então há [", (i * protocolo), "] micro-erros a serem cometidos")
      escreval("")
   fimpara
   
   timer 50
   Separador
   Enter

   escreval("")
   timer 1500
   escreval("Iniciando a próxima etapa...")
   timer 2000
   timer 50
   limpatela
fimprocedimento
//=========================
procedimento ExercicioCinco
inicio

   Separador
   escreval("Digite 10 protocolos e descubra se há algum grande erro em neles")

   para i de 1 ate 10 passo 1 faca
      leia(protocolo)
      se (protocolo / 2 = protocolo \ 2 ) entao
          escreval("No protocolo Nº", protocolo, " não há nenhum erro(par).")
      senao
           escreval("No protocolo Nº", protocolo, " há um grande erro(impar).")
      fimse
   fimpara

   escreval("")
   timer 1500
   escreval("Iniciando a próxima etapa...")
   timer 2000
   timer 50
   limpatela

fimprocedimento
//=========================
procedimento ExercicioExtra
inicio
   limpatela
   Separador
   timer 500
   escreval("Calculadora Simples Iniciada!!")
   timer 50
   
   escreval("Digite:")
   escreval("1 - Adição/+")
   escreval("2 - Subtração/-")
   escreval("3 - Multiplicação/*")
   escreval("4 - Divisão/%")
   escreval("5 - Potência Quadratica/Elevação ao quadrado")
   escreval("6 - Sair")
   leia(decidaExtra)
escolha decidaExtra
   caso 1
   DigiteDoisNumeros
   escreval(num1, " +", num2, " =", (num1 + num2))
   
   Enter
   ExercicioExtra
   caso 2
   DigiteDoisNumeros
   escreval(num1, " -", num2, " =", (num1 - num2))

   Enter
   ExercicioExtra
   caso 3
   DigiteDoisNumeros
   escreval(num1, " *", num2, " =", (num1 * num2))

   Enter
   ExercicioExtra
   caso 4
       escreval("Digite o primeiro número.")
       leia(num1)
       escreval("Digite o segundo número.")
       repita
       leia(num2)
       ate (num2 <> 0)
       
   escreval(num1, " /", num2, " =", (num1 / num2))

   Enter
   ExercicioExtra
   caso 5
   escreval("Digite o primeiro número.")
   leia(num1)
   escreval(num1, "²", " =", (num1 * num1))

   Enter
   ExercicioExtra
   caso 6
   escreval("Saindo da Calculadora Simples...")
   timer 1000
   timer 50
   outrocaso
fimescolha

   escreval("")
   timer 1500
   escreval("Desligando...")
   timer 2500
   escreval("Foi bom te conhecer...")
   timer 5
   limpatela

fimprocedimento
//=========================
procedimento Exercicios
inicio
      ExercicioUm
      ExercicioDois
      ExercicioTres
      ExercicioQuatro
      ExercicioCinco
      ExercicioExtra
fimprocedimento
//Procedimento "Exercicios" criado para facilitar chamar todos os Exercicios
//E também porque dentro dele existe o nome funcional para cada Exercicio
// ==========================================================================
// ==========================================================================
// ==========================================================================
Inicio
      Exercicios
      









Fimalgoritmo
