# **Detecção Inteligente de Malware com Python**

Por Luís Gustavo Martins Amaral Alécio Gomes

GitHub: [luisgustavo02](https://github.com/luisgustavo02)

Email: [lg.amaral.02@gmail.com](mailto:lg.amaral.02@gmail.com)

Email: [luis.gustavomartins@ufpe.br](mailto:luis.gustavomartins@ufpe.br)

Essa apresentação foi baseada na ação de extensão da UFPE, desenvolvida pelo prof. Sidney Lima em parceria com escolas públicas na Região Metropolitana de Recife. Mais informações sobre o projeto podem ser encontradas abaixo:

Site: [UFPE - Segurança Extensão](https://sites.ufpe.br/seguranca-extensao/)

Email: [sidney.lima@ufpe.br](mailto:sidney.lima@ufpe.br)

---

## **1. Apresentação:**

<img src="docs/images/luisgustavo.png" width="200" height="200" alt="Luís Gustavo">

Meu nome é Luís Gustavo, tenho 24 anos e sou natural de Maceió, Alagoas. Também sou estudante de Engenharia Eletrônica na UFPE, em Recife, com formação prevista para o final de 2026.

Atualmente, faço parte do grupo de pesquisa [Computação Biomédica](https://sites.ufpe.br/computacaobiomedica/) como pesquisador CNPq e também faço pesquisa no Laboratório de Aplicações em Processamento de Sinais, do Departamento de Eletrônica e Sistemas (DES) da UFPE.

Sou pós-júnior da Dipolum Consultoria, empresa júnior de Engeharia Eletrônica, e fui monitor de disciplinas como Computação Eletrônica, Segurança da Informação e Medidas Eletromagnéticas ao longo da graduação. Nos últimos períodos, entrei no Diretório Acadêmico do DES e ministrei aulas sobre introdução a Linguagem C e Python voltadas para novos discentes.

---

## **2. Introdução:**

Nos conceitos de segurança da informação, o termo **malware** (em inglês, software malicioso) é uma expressão geral para descrever programas desenvolvidos com o intuito de causar danos, obter acessos não autorizados, roubar informações, comprometer a segurança do dispositivo ou interromper serviços. **Malwares** podem infectar computadores, notebooks, smartphones, servidores e até dispositivos da Internet das Coisas (IoT).

Dentre os principais tipos de **malwares**, podemos destacar:

- **Vírus**: Malwares do tipo vírus tem o objetivo de infectar o computador, replicar-se e espalhar-se. Essa replicação e espalhamento ocorre por meio de ações do usuário, como abrir um arquivo infectado.

- **Ransomware**: O ransomware é o tipo de programa malicioso que criptografa os dados da máquina e faz extorsão, frequentemente pedindo pagamentos por meio de bitcoins. Em caso de não pagamento, os dados eram apagados do computador.

- **Spyware**: É um programa malicioso que coleta dados do usuário sem o conhecimento, seja via tela (screenlogger) ou teclado e mouse (keylogger).

- **Rootkit**: Rootkit, do inglês root (administrador) e kit (conjunto de ferramentas), é um malware que permite o acesso de administrador a outros programas maliciosos.

- **Backdoor**: Backdoor é um software que burla as regras de segurança convencionais para dar acesso remoto a outro dispositivo.

- **Worms**: Worms são um tipo de malware que se replicam e se espalham por meio da rede de computadores, sem a necessidade de ação humana.

Ao longo da história dos computadores, tivemos alguns casos famosos no mundo, a exemplo do vírus ILOVEYOU (maio de 2000), do ransomware WannaCry (12 de maio de 2017) e do spyware Pegasus.

<img src="docs/images/wannacry_ransomware.png" width="500" height="500" alt="Imagem da tela do ransomware WannaCry">

---

## **3. Análise Estática de Malware:**

A análise estática de malware corresponde ao estudo de um programa por meio de ferramentas de estudo, como engenharia reversa, de uma maneira que o software malicioso não é executado e estudado em tempo real. Com essa técnica, é possível identificar o modus operantis do malware.

Como exemplo, podemos utilizar dois métodos para realizar a análise estática de programas maliciosos:

### **3.1. Androwarn:**

O [Androwarn](https://github.com/jok22/androwarn) é um programa de código-aberto escrito em Python para a detecção e análise de malwares para dispositivos Android. A principal referência desse código é a biblioteca **[androguard](https://github.com/androguard/androguard)**.

Para este exemplo, temos a seguinte base de dados https://github.com/DejavuForensics/AndroidSamples de malwares para Android.

Iniciando a parte prática, precisamos clonar o repositório com o comando:

`git clone https://github.com/DejavuForensics/AndroidSamples`

ou baixar o arquivo .ZIP e extraí-lo. Após isso, podemos clonar o repositório do Androwarn:

`git clone https://github.com/jok22/androwarn`

Feita a instalação, podemos entrar no modo root ou administrador, criar um ambiente virtual e ativá-lo com o Python.

```cmd
sudo su
python -m venv venv
source venv/bin/activate
```

Já no ambiente virtual criado, podemos acessar o diretório do androwarn e instalar as bibliotecas necessárias.

```cmd
cd androwarn
pip install -r requirements.txt
```

Por fim, temos os parâmetros principais para executar o código do androwarn:

- `-i`: Abreviatura para *input*, indicando o caminho do arquivo **.APK** de entrada.

- `-r`: Abreviatura para *report*, indicando o formato do relatório, em que o valor padrão é html (txt; html; json).

- `-v`: Abreviatura para *verbose*, indicando o nível de especificidade, em que valor padrão é 1 (Essencial 1; Avançado 2; Perito 3).

Assim, executamos o comando, selecionando um dos malwares da pasta:

`python androwarn.py -i AndroidSamples-main/VirusShare... -r html -v 3`


### **3.2. PEscanner:**

---

## **4. Análise Dinâmica de Malware:**

Em contrapartida, a análise dinâmica de malware trata um programa malicioso em um ambiente controlado, sendo devidamente configurado, para que os comportamentos do software e do sistema sejam observados.

---

## **5. Extração de Features:**

---

## **6. Machine Learning Aplicado:**

---

## **7. Demonstração em Python:**

---

## **8. Resumo e Conclusão:**
