# Projeto_sistema_RH
Projeto de sistema de RH, trabalho de curso.

#include <iostream>
#include <string>

int main () {
    std::string nome;
    int ano, mes, ano_total, mes_total, tempo_total, opcao, ferias;
    float salario;

std::cout << "Insira seu nome: "<< std::endl;
std::cin.ignore();
std::getline(std::cin, nome);
while(true){

std::cout << "Escolha uma das opções: \n (Escolha pelo número referente a opção) \n 1 - Aumento de Salário. \n 2 - Processo Seletivo \n 3 - Férias \n 4 - Calculo 13º \n 5 - sair "<< std::endl;
std::cin >> opcao;

    if (opcao == 1) {
        std::cout << "Insira quanto tempo desde o ultimo aumento salarial. (caso não teve ainda, insira o tempo de casa). \n (separando ano de meses, exemplo: Anos: 2, Meses: 4)" << std::endl;
        std::cout << "Anos: " << std::endl;
        std::cin >> ano;
        std::cout << "Meses: " << std::endl;
        std::cin >> mes;
        ano_total = ano*365;
        mes_total = mes*30;
        tempo_total = ano_total+mes_total;
            
            if (tempo_total > 365 && tempo_total <= 730)
                std::cout << "O funcionário poderá solicitar junto ao RH um aumento de 10%" << std::endl;
            else if (tempo_total > 730)
                std::cout << "O funcionário poderá solicitar junto ao RH um aumento de 20%" << std::endl;
            else
                std::cout << "Segundo as regras do RH, o funcionário ainda não está apto a solicitar o aumento" << std::endl;
        }
        
    else if (opcao == 2){
        std::cout << "Insira quanto tempo desde a ultima participação do processo seletivo. (caso não tenha participado de nenhum, insira o tempo de casa). \n (separando ano de meses, exemplo: Anos: 2, Meses: 4)" << std::endl;
        std::cout << "Anos: " << std::endl;
        std::cin >> ano;
        std::cout << "Meses: " << std::endl;
        std::cin >> mes;
        ano_total = ano*365;
        mes_total = mes*30;
        tempo_total = ano_total+mes_total;
        
        if (tempo_total > 150)
                std::cout << "O funcionário poderá solicitar a participação do processo seletivo." << std::endl;
            else
                std::cout << "Segundo as regras do RH, o funcionário ainda não poderá participar do processo seletivo." << std::endl;
        }
        
    else if (opcao == 3){
        std::cout << "Insira o tempo de empresa. \n (separando ano de meses, exemplo: Anos: 2, Meses: 4)" << std::endl;
        std::cout << "Anos: " << std::endl;
        std::cin >> ano;
        std::cout << "Meses: " << std::endl;
        std::cin >> mes;
        ano_total = ano*365;
        mes_total = mes*30;
        tempo_total = ano_total+mes_total;
        std::cout << "Quantas férias já tirou?. \n (Caso não tenha tirado férias ainda, insira 0.)" << std::endl;
        std::cin >> ferias;
        
        if (tempo_total > 365 && ferias == 0)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else if (tempo_total > 730 && ferias <= 1)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else if (tempo_total > 1095 && ferias <= 2)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else if (tempo_total > 1460 && ferias <= 3)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else if (tempo_total > 1825 && ferias <= 4)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else if (tempo_total > 2190 && ferias <= 5)
                std::cout << "O funcionário já poderá solicitar as férias." << std::endl;
            else
                std::cout << "O funcionário ainda não possui disponibilidade para solicitar as férias." << std::endl;
        } 
    else if (opcao == 4){
        std::cout << "Insira o mês que entrou na empresa pelo número, sendo: \n 1 - Janeiro \n 2 - Fevereiro \n 3 - Março \n 4 - Abril \n 5 - Maio"
        "\n 6 - Junho \n 7 - Julho \n 8 - Agosto \n 9 - Setembro \n 10 - Outubro \n 11 - Novembro \n 12 - Dezebro"<< std::endl;
        std::cin >> mes;
        std::cout << "Caso ja tenha mais de 1 ano, insira quantos anos tem de empresa: \n Caso não tenha 1 ano ainda, insira zero: " << std::endl;
        std::cin >> ano;
        std::cout << "Insira o valo do seu salário: " << std::endl;
        std::cin >> salario;
        
        if (ano > 0)
                std::cout << "O valor a receber é de: R$ " << salario<< std::endl;
            else if (ano == 0 && mes == 1)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*11<< std::endl;
            else if (ano == 0 && mes == 2)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*10<< std::endl;
            else if (ano == 0 && mes == 3)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*9<< std::endl;
            else if (ano == 0 && mes == 4)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*8<< std::endl;
            else if (ano == 0 && mes == 5)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*7<< std::endl;
            else if (ano == 0 && mes == 6)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*6<< std::endl;
            else if (ano == 0 && mes == 7)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*5<< std::endl;
            else if (ano == 0 && mes == 8)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*4<< std::endl;
            else if (ano == 0 && mes == 9)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*3<< std::endl;
            else if (ano == 0 && mes == 10)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*2<< std::endl;
            else if (ano == 0 && mes == 11)
                std::cout << "O valor a receber é de: R$ " << (salario/12)*1<< std::endl;
            else if (ano == 0 && mes == 12)
                std::cout << "Não está apto a receber o 13º"<< std::endl;
            else
                std::cout << "Valor inválido" << std::endl;
        } 
        else if (opcao == 5){
            return 0;
        }
    else
        std::cout << "Opção Inválida" << std::endl;
        
    }
}
