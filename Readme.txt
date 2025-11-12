
---

## 🧠 Discussão Física

- A diferença de pressão entre extrados e intrados, evidenciada pelo gráfico de Cp, confirma a geração de sustentação.
- O rastro de baixa velocidade a jusante está diretamente relacionado ao arrasto aerodinâmico.
- O modelo k–ω SST mostrou-se adequado para capturar zonas de separação e garantir estabilidade numérica.
- A malha com y⁺ ≈ 1 permitiu resolução precisa da camada limite, essencial para confiabilidade dos coeficientes.

---

## 🧑‍💻 Sobre mim

Este projeto foi desenvolvido por **Paulo**, estudante e entusiasta de simulação computacional e engenharia de escoamentos. A execução envolveu domínio prático do ANSYS Fluent, conhecimento teórico em dinâmica dos fluidos e organização técnica para apresentação em portfólio.


# 💨 Simulação CFD do Perfil Aerodinâmico NACA 0012 com ANSYS Fluent

Este projeto apresenta uma simulação computacional completa do escoamento sub-sônico incompressível
sobre o perfil aerodinâmico **NACA 0012**, utilizando o software **ANSYS Fluent**. 
O estudo foi conduzido com foco em precisão física, refinamento de malha e análise de sustentação e arrasto, 
integrando conhecimentos teóricos de dinâmica dos fluidos com práticas avançadas de CFD. Durante a elaboração foram feitas pesquisas aprofundadas, 
estudos por meios de mecânismos de aprendizado tais como livros, artigos, sites, videos aulas em plataformas divulgação e cursos onlines.
Assim que possível incluirei todo o material utilizado para que todos os estudantes e entusiastas possam também se aprofundar nestes tópicos.

---

## 🎯 Objetivo

Investigar o comportamento aerodinâmico do perfil NACA 0012 em regime laminar-turbulento, 
quantificando os coeficientes de sustentação (CL) e arrasto (CD), e analisando a distribuição de pressão e velocidade no entorno do perfil.

---

## ⚙️ Parâmetros de Simulação

| Parâmetro                  | Valor                          |
|---------------------------|--------------------------------	|
| Perfil                    | NACA 0012                      	|
| Regime                    | Sub-sônico incompressível (Ma<0.3)|
| Número de Reynolds (Re)   | \(1.5 \times 10^5\)            	|
| Fluido                    | Ar (\(\rho = 1.225\) kg/m³), L=1m, &mu=1.81e-5 Kg(m*s)    	|
| Velocidade de entrada     | 88.65 m/s                       	|
| Modelo de turbulência     | Spalart-Allmarus Turbulent Model                        	|
| Domínio computacional     | Canal 2D (6c frente, 10c trás, 5c acima/abaixo) |
| y⁺ alvo                   | ~1                             |
| Espessura da 1ª camada    | 0.1141 mm                      |

---

## 🧩 Etapas Realizadas

### 1. Geometria e Domínio
- Importação das coordenadas do NACA 0012 via UIUC Airfoil Database
- Construção do domínio de escoamento 2D no SpaceClaim
- Nomeação das fronteiras para definição de condições de contorno

### 2. Malha
- Malha estruturada com refinamento na parede do perfil
- Camadas de inflação para captura da camada limite
- Verificação de qualidade: Orthogonal Quality > 0.1

### 3. Configuração no Fluent
- Solver baseado em pressão, regime estacionário, 2D
- Modelo Spalart-Allamarus para robustez em regiões de separação
- Inicialização híbrida e discretização de segunda ordem

### 4. Monitoramento e Convergência
- Monitores de CL e CD configurados na parede do perfil
- Critério de convergência: resíduos \(10^{-6}\) e estabilidade dos coeficientes

---

## 📊 Pós-processamento e Resultados

### 🔵 Contornos
- **Pressão**: evidência da diferença entre extrados e intrados
- **Velocidade**: aceleração sobre o perfil e rastro de baixa velocidade
- **Linhas de corrente**: padrão de escoamento e zonas de recirculação

### 📈 Gráficos
- **Cp vs x/c**: distribuição de pressão ao longo da corda
Os dois gráficos abaixo serão feitos no projeto seguinte a este.
- **CL vs α**: variação da sustentação com o ângulo de ataque
- **CD vs CL**: eficiência aerodinâmica

### 📄 Relatórios
- Exportação dos valores finais de CL e CD
Os dados estão sendo organizados e tratados para análise em Python. Estarão disponíveis em um projeto separado.
- Dados organizados para análise em Excel/Python

---

## 📁 Organização dos Arquivos

