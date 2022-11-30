cal=0
nome, cpf, end, tele, email, senha = ("", "", "", "", "", "")
arquivo = open("arquivo1.txt", "r")
arquivo.close()
def enviarDados(dados):
    arquivo = open("arquivo1.txt", "w+")
    arquivo.write("%s" %dados)
    arquivo.close()
def lerDados():
    arquivo = open("arquivo1.txt", "r")
    return eval(arquivo.read())
dados_total = lerDados()
while True :
    print('========================MENU DE CADASTRO========================')
    print('1-Cadastro')
    print('2-Ler')
    print('3-Deletar')
    print('4-Atualizar')
    print('5-Sair')
    a = int(input("Escolha sua opção: "))
    if a == 1 :
        if cal <= 5 :
            arquivo = open("arquivo1.txt", "w+")
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total.append([nome, cpf, end, tele, email, senha])
            enviarDados(dados_total)
        else :
            print('limite estourado')

    if a == 2 :
        print("========================DADOS ATUAIS========================")
        for el in dados_total:
            print("Nome: ", el[0])
            print("CPF: ", el[1])
            print("ENDEREÇO: ", el[2])
            print("TELEFONE: ", el[3])
            print("EMAIL: ", el[4])
            print("SENHA: ", el[5])
            print("\n")
    if a == 3:
        if (len(dados_total) >= 1):
            print('1 - Cadastro 1')
        if (len(dados_total) >= 2):
            print('2 - Cadastro 2')
        if (len(dados_total) >= 3):
            print('3 - Cadastro 3')
        if (len(dados_total) >= 4):
            print('4 - Cadastro 4')
        if (len(dados_total) >= 5):
            print('5 - Cadastro 5')
        esc = int (input("Qual dado você deseja deletar: "))
        if esc == 1:
            dados_total.pop(0)
            enviarDados(dados_total)
        if esc == 2:
            dados_total.pop(1)
            enviarDados(dados_total)
        if esc == 3:
            dados_total.pop(2)
            enviarDados(dados_total)
        if esc == 4:
            dados_total.pop(3)
            enviarDados(dados_total)
        if esc == 5:
            dados_total.pop(4)
            enviarDados(dados_total)
    if a == 4 :
        if (len(dados_total) >= 1):
            print('1 - Cadastro 1')
        if (len(dados_total) >= 2):
            print('2 - Cadastro 2')
        if (len(dados_total) >= 3):
            print('3 - Cadastro 3')
        if (len(dados_total) >= 4):
            print('4 - Cadastro 4')
        if (len(dados_total) >= 5):
            print('5 - Cadastro 5')
        ec = int (input("Qual dado você deseja atualizar: "))
        if ec == 1:
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total[0]=nome,cpf,end,tele,email,senha
            arquivo=open("arquivo1.txt", "w")
            arquivo.writelines("%s"%dados_total)
            enviarDados(dados_total)
            arquivo.close
        if ec == 2:
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total[1]=nome,cpf,end,tele,email,senha
            arquivo=open("arquivo1.txt", "w")
            arquivo.writelines("%s"%dados_total)
            enviarDados(dados_total)
            arquivo.close
        if ec == 3:
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total[2]=nome,cpf,end,tele,email,senha
            arquivo=open("arquivo1.txt", "w")
            arquivo.writelines("%s"%dados_total)
            enviarDados(dados_total)
            arquivo.close
        if ec == 4:
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total[3]=nome,cpf,end,tele,email,senha
            arquivo=open("arquivo1.txt", "w")
            arquivo.writelines("%s"%dados_total)
            enviarDados(dados_total)
            arquivo.close
        if ec == 5:
            nome = input('Nome: ')
            cpf = input('Cpf: ')
            end = input("Endereço: ")
            tele = input("Telefone: ")
            email = input("Email: ")
            senha = input("Senha: ")
            dados_total[4]=nome,cpf,end,tele,email,senha
            arquivo=open("arquivo1.txt", "w")
            arquivo.writelines("%s"%dados_total)
            enviarDados(dados_total)
            arquivo.close
    if a == 5 :
        print('Fechando sistema')
        print('by: Júnior Hora & Paulo Henrique Gomes')
        quit()
    if a <=0 and a > 5:
      print("Opção Inválida")
