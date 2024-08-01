def bemVindo():
    print("-"*51)
    print("Bem-vindo! Vamos calcular as notas dos alunos(as)?")
    print("-"*51)
    print()



def validaNota(prompt, valorMin, valorMax): ##função para input e validação das notas
    while True:
        try:
            notaAtividade = float(input(prompt))
            if valorMin <= notaAtividade <= valorMax:
                return notaAtividade
            else:
                print()
                print(f"Valor inválido para esta atividade! Digite um valor entre 0 e {valorMax}: ")
                print()

        except ValueError:
            print()
            print("Valor inválido, tente novamente!")
            print()


##função main onde solicita o input e a validação da aprovação do aluno, também valida a quantidade de aprovados.

def main():
    bemVindo()

    totalAlunos = 100
    aprovados = 0
    reprovados = 0

    for i in range(totalAlunos): ##input de notas
        aop1 = validaNota(f"Insira a nota do aluno(a) {i+1} na Atividade Online Pontuada 1 [0,1]: ", 0, 1)
        aop2 = validaNota(f"Insira a nota do aluno(a) {i+1} na Atividade Online Pontuada 2 [0,2]: ", 0, 2)
        aop3 = validaNota(f"Insira a nota do aluno(a) {i+1} na Atividade Online Pontuada 3 [0,1]: ", 0, 1)
        provaReg = validaNota(f"Insira a nota do aluno(a) {i+1} na Prova Regular [0,6]: ", 0, 6)
        print()

        somaModulo = aop1 + aop2 + aop3 + provaReg ##calcula total da soma das notas
        print(f"Aluno(a) obteve a nota '{somaModulo}' nesse módulo.")


        if somaModulo >= 7.0: ##valida a aprovação
            status = "Aprovado."
            aprovados +=1
        else:
            print("Aluno(a) não atingiu a nota de aprovação!")
            notaRec = validaNota("Insira a nota do aluno(a) na Recuperação [0,10]: ", 0, 10)
            mediaModulo = (somaModulo + notaRec) / 2 ##calcula total da soma das notas incluindo a recuperação
            if mediaModulo >= 5.0:
                print(f"Aluno(a) obteve a nota '{mediaModulo}' nesse módulo.")
                status = "Aprovado."
                aprovados += 1
            else:
                print(f"Aluno(a) obteve a nota '{mediaModulo}' nesse módulo.")
                status = "Reprovado."
                reprovados += 1

        print(f"Aluno(a) {i+1} está: {status}")
        print()

    print(f"Total de alunos: {totalAlunos}")
    print()

    ##valida porcentagem de aprovados
    print(f"Aprovados: {(aprovados / totalAlunos) * 100:.2f}%")
    print(f"Aprovados: {(reprovados / totalAlunos) * 100:.2f}%")




main()
