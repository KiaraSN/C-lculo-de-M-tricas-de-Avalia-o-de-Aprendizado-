# Cálculo-de-Métricas-de-Avaliação-de-Aprendizado-
Descrição do Projeto

Neste projeto, implementamos funções em Python para calcular as principais métricas de avaliação de modelos de classificação de dados. O objetivo é entender o funcionamento de cada métrica e como elas podem ser aplicadas a diferentes modelos.

As métricas implementadas incluem:

Acurácia

Sensibilidade (Recall)

Especificidade

Precisão (Precision)

F-score

Para o cálculo dessas métricas, utilizamos valores de VP, VN, FP e FN obtidos a partir de uma matriz de confusão. Neste projeto, a matriz de confusão foi escolhida de forma arbitrária apenas para fins didáticos.

Métricas e Fórmulas
Métrica	Fórmula	Descrição
Sensibilidade	VP / (VP + FN)	Proporção de positivos corretamente identificados
Especificidade	VN / (VN + FP)	Proporção de negativos corretamente identificados
Precisão	VP / (VP + FP)	Proporção de predições positivas corretas
Acurácia	(VP + VN) / N	Proporção de predições corretas no total
F-score	2 × (Precisão × Sensibilidade) / (Precisão + Sensibilidade)	Média harmônica entre precisão e sensibilidade

Legenda:

VP: Verdadeiros Positivos

VN: Verdadeiros Negativos

FP: Falsos Positivos

FN: Falsos Negativos

N: Total de exemplos

P: Precisão

S: Sensibilidade

Estrutura do Código

Definição da matriz de confusão (VP, VN, FP, FN).

Implementação de funções para cada métrica:

sensibilidade(vp, fn)

especificidade(vn, fp)

precisao(vp, fp)

acuracia(vp, vn, fp, fn)

f_score(precisao, sensibilidade)

Cálculo e impressão das métricas usando a matriz de confusão escolhida.

Exemplo de Uso
# Matriz de confusão de exemplo
VP, VN, FP, FN = 40, 50, 10, 5

# Cálculo das métricas
sen = sensibilidade(VP, FN)
esp = especificidade(VN, FP)
prec = precisao(VP, FP)
acc = acuracia(VP, VN, FP, FN)
fsc = f_score(prec, sen)

# Impressão dos resultados
print(f"Sensibilidade: {sen:.2f}")
print(f"Especificidade: {esp:.2f}")
print(f"Precisão: {prec:.2f}")
print(f"Acurácia: {acc:.2f}")
print(f"F-score: {fsc:.2f}")

Conclusão

Este projeto permite compreender como cada métrica reflete o desempenho do modelo de classificação, útil para análises exploratórias e comparações entre diferentes algoritmos de aprendizado supervisionado.
