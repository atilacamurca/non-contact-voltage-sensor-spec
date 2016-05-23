# Introdução

Este sensor tem o objetivo de detectar tensão em um fio sem o contato com o mesmo.
Com isso você pode testar se há tensão nos fios de aparelhos elétricos, em fios
de uma tubulação em que você não encontre a saída ou simplesmente para detectar
eletricidade estática de um corpo.

# Material Utilizado

* Protoboard
* Fios
* 1 LED Vermelho Standard
* 1 Bateria de 9V
* 3 Transistores modelo BC546 - B (NPN)
* 1 Resistor de 220 $\Omega$
* 1 Resistor de 100K $\Omega$
* 1 Resistor de 1M $\Omega$
* 1 Push Button

## Informações sobre o Transistor BC546

* Pacote TO-92
* $V_{CBO} = 80V$
* $V_{CEO} = 65V$
* $V_{EBO} = 6V$
* $I_C = 100mA$ - Corrente do Coletor
* $P_C = 500mW$ - Potência do Coletor
* $T_J = 150 \degree C$ - Temperatura da Junção
* $H_{FE} = 200 \sim 450$ - Classificação B

# Montagem do Circuito

\begin{figure}[H]
	\includegraphics[scale=0.9]{img/non-contact-voltage-sensor_bb.jpg}
	\caption{Montagem Visão Protoboard}
\end{figure}

## Esquemático

\begin{figure}[H]
	\includegraphics[scale=1.6]{img/non-contact-voltage-sensor_Esquematico.jpg}
	\caption{Esquemático}
\end{figure}

# Funcionamento

A ideia básica de funcionamento é a seguinte: Ao acionar o _Push Button_ o sistema
é energizado e está preparado para detectar tensão. Para isso é utilizado uma espécie
de antena, a qual ao estar próxima a uma fonte de tensão em que há um campo
eletromagnético, potencializa essa tensão no circuito fazendo com que o LED acenda.

Os Transistores servem como chaves e também tem a função de elevar a tensão.
Se você usar a saída de um transistor para controlar outro, o ganho multiplica.
Com dois transistores, o ganho ideal ($H_{FE} = 200$) torna-se $200 \times 200 = 40000$,
com 3 transistores, o ganho chega a $200 \times 200 \times 200 = 8000000$! É um ganho
altíssimo e permite que o circuito seja usado para detectar o menor dos movimentos
de eletricidade - mesmo aqueles criados à distância por indução ou eletricidade estática!

# Conclusão

Com um circuito simples com zero de programação por software é possível criar um
detector de tensão usando somente a física. Com esse exemplo prático é possível
comprovar a existência de campos eletromagnéticos.

**Observação**: Apesar de tudo não use este circuito em equipamentos de alta tensão,
mesmo que ele indique que não há tensão. Você pode correr riscos ao manipular estes
equipamentos. Na dúvida evite o contato.

Também não utilize perto de fios desencapados, ou diretamente no plug da tomada.
Também a riscos de choque nesses casos.





