# Verificação de Serviços Contratados em Java

Projeto em Java criado para verificar se um cliente contratou um serviço específico. Ele utiliza entrada de dados pelo terminal e manipulação de strings para determinar se o serviço está listado entre os contratados pelo cliente.

## 🛠 Funcionalidades

- Recebe o nome de um serviço a ser verificado.
- Recebe o nome do cliente e a lista de serviços contratados separados por vírgulas.
- Retorna "Sim" se o serviço está na lista de serviços contratados, ou "Nao" caso contrário.

## Estrutura do Código

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Entrada do serviço a ser verificado
        String servico = scanner.nextLine().trim();

        // Entrada do nome do cliente e os serviços contratados
        String entradaCliente = scanner.nextLine().trim();

        // Separando o nome do cliente e os serviços contratados
        String[] partes = entradaCliente.split(",");
        boolean contratado = false;

        // TODO: Verifique se o serviço está na lista de serviços contratados
        for (int i = 1; i < partes.length; i++) {
            if (partes[i].trim().equals(servico)) {
                contratado = true;
                break;
            }
        }

        // Saída do resultado
        if (contratado) {
            System.out.println("Sim");
        } else {
            System.out.println("Nao");
        }

            scanner.close();
    }
}
