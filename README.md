- 👋 Hi, I’m @Leandroppqpq
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Leandroppqpq/Leandroppqpq is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
using namespace std;

int main() {
    int fraldas_coletadas = 0;
    bool derrotou_monstros = false;
    bool encontrou_marido = false;
    bool ganhou_bebê = false;

    cout << "Bem-vindo ao jogo da Millena!" << endl;

    while (fraldas_coletadas < 2023) {
        cout << "Você está em uma floresta cheia de monstros. O que deseja fazer?" << endl;
        cout << "1. Lutar contra um monstro" << endl;
        cout << "2. Procurar por fraldas" << endl;
        cout << "3. Encontrar o Leandro" << endl;
        cout << "4. Sair do jogo" << endl;

        int opcao;
        cin >> opcao;

        switch (opcao) {
            case 1:
                if (!derrotou_monstros) {
                    cout << "Você derrotou um monstro!" << endl;
                    derrotou_monstros = true;
                } else {
                    cout << "Você já derrotou todos os monstros da floresta!" << endl;
                }
                break;
            case 2:
                if (!derrotou_monstros) {
                    cout << "Você precisa derrotar os monstros antes de procurar por fraldas!" << endl;
                } else {
                    cout << "Você encontrou algumas fraldas!" << endl;
                    fraldas_coletadas += 100;
                }
                break;
            case 3:
                if (!encontrou_marido) {
                    cout << "Você encontrou o Leandro!" << endl;
                    encontrou_marido = true;
                } else {
                    cout << "Você já encontrou o Leandro!" << endl;
                }
                break;
            case 4:
                cout << "Saindo do jogo..." << endl;
                return 0;
            default:
                cout << "Opção inválida. Por favor, escolha novamente." << endl;
                break;
        }

        if (fraldas_coletadas >= 2023 && !ganhou_bebê && encontrou_marido) {
            cout << "Parabéns, você coletou 2023 fraldas e ganhou a bebê Merllya!" << endl;
            ganhou_bebê = true;
        }
    }

    cout << "Você coletou todas as fraldas necessárias. Obrigado por jogar!" << endl;

    return 0;
}
