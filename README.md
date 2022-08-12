# taxa-metabolica-basal-calculator
# Calculadora de Dieta (Calcula calorias a serem consumidas no dia a dia, para emagrecer, manter o corpo ou ganhar massa )


peso = float(input('Qual a seu peso? '))

altura = float(input('Qual a sua altura? '))

idade = float(input('Qual a sua idade? '))

sexo = str(input('Qual seu genero? (FEMININO OU MASCULINO) ')).upper().strip()[0]

constante = 0;

if sexo == "feminino":

    constante = -161
    
    
else:

    constante = 5
    

result = ((10*peso)+(6.25*altura)-(5*idade) + constante)


print('Sua Taxa Metabólica Basal é {}'.format(result))


print('''A TAXA METABÓLICA BASAL (TMB) é minimo de energia necessária para as
funções do organismo em repouso, como batimentos cardíacos, pressão arterial, 
a respiração e a manutenção da temperatura corporal.''')


ex = str(input('Qual seu nível de exercícios? (SEDENTARIO, LEVE, MODERADO, INTENSO OU ATLETA ) ')).upper().strip()[0]


const1 = 0

sedentario = 1.2

leve = 1.375

moderado = 1.55

instenso = 1.725

atleta = 1.9


if ex =='sedentario':

    const1 = 1.2
    print('Seu Gasto Energético total é: {:.1f}'.format(result*const1))

if ex =='leve':

    const1 = 1.375
    print('Seu Gasto Energético Total é {:.1f}'.format(result*const1))

if ex == 'moderado':
    const1 = 1.55
    print('Seu Gasto Energético Total é {:.1f}'.format(result*const1))

if ex == 'intenso':
    const1 = 1.725
    print('Seu Gasto Energético Total é {:.1f}'.format(result*const1))

if ex == 'atleta':
    const1 = 1.9
    print('Seu Gasto Energético Total é {:.1f}'.format(result*const1))
    
print('''O Gasto Energético Total ou GET é seu gasto energético diário TMB com todas as atividades que você faz 
durante o dia.''')

get1 = (result*const1)-500

get = result*const1

get2 = result*const1+500

print('Para perder peso você deve consumir {:.2f}, que é um déficit de 500 calorias por dia da sua manutenção.'.format((get1)))

print('Para manter o peso você deve consumir, {:.2f}.'.format(get))

print('Para ganhar peso você deve consumir {:.2f}, que é um aumento de 500 calorias por dia da sua manutenção.'.format( get2 ))

