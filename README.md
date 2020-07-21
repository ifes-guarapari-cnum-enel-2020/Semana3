# Semana3
![](https://github.com/ifes-guarapari-cnum-enel-2020/Semana3/workflows/Julia%20CI/badge.svg)

Atividades Pedagógicas Não Presenciais

## Fundamentos de linguagem de programação
Para continuidade do aprendizado sobre a linguagem Julia, é importante conhecer os comandos de entrada e saída, variáveis, bibliotecas, cálculos, condicionais, repetições, funções, vetores e matrizes.

Vamos declarar e usar variáveis e funções, realizando operações matemáticas. As funções podem ser escritas como na matemática ou como na programação, em que se permite o uso de comandos.
```julia
v = 1

println(v)

f(x) = x^2 + x + 1

z = f(v)

println(z)

function fx(x, a, b, c)
 y(n) = a*n^2 + b*n + c
 return y(x)
end

z = fx(1,2,3,4)

println(z)
```

Os condicionais podem ser usados dentro das funções para a lógica da programação e o retorno da função pode não existir (nothing), pode ser um número ou um vetor, que é expresso usando colchetes.
```julia
function zero(a, b, c)
 if a != 0
  delta = (b^2)-(4*a*c)
  if delta > 0
   x1 = (-b+sqrt(delta))/(2*a)
   x2 = (-b-sqrt(delta))/(2*a)
   return [x1 x2]
  end
 else
  return -c/b
 end
end

v = [1 2 3]
z = zero(1,2,3)
println(z)
z = zero(1,4,2)
println(z)
println(z[1])
```

As matrizes são também declarados como colchetes e para separação de linhas usa-se o ponto e vírgula. Tanto linhas como colunas podem ser vistas como vetores, facilitados por operadores.
```julia
m = [-2 5 1 ;
     -1 4 0]

println(m)
println(m[1,1])
println(m[:,1])
println(m[1,:])

for v = eachrow(m)
 println(v)
 println(v[1])
end
```
