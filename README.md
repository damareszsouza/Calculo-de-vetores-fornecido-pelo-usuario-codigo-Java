# Calculo-de-vetores-fornecido-pelo-usuario-codigo-Java

Considere o seguinte problema:

Elabore um programa que, dados dois vetores inteiros de 10 posições, efetue as respectivas operações indicadas por outro vetor de 10 posições de caracteres, também fornecido pelo usuário, contendo os símbolos das quatro operações aritméticas básicas em qualquer combinação e armazenando os resultados em um terceiro vetor. Por exemplo, se a posição 2 do primeiro vetor contiver 10, a posição 2 do segundo vetor contiver 2 e a posição 2 do vetor de operações contiver “-”, a posição 2 do vetor de resultados deverá ter 8.

Complete o programa abaixo de forma que implemente corretamente o problema acima.



public class VetoresOperacoes {
	public static void main(String[] args) {
		[int[] vetorA = new int[10];]
		int[] vetorB = new int[10];
		int[] resultados = new int[10];
		char[] op = new char[10];
		
		// Leitura
		for(int cont = 0; cont < vetorA.length; cont++) {
			System.out.printf("Vetor A posicao %d: ", cont);
			[vetorA[cont] = Integer.parseInt(System.console().readLine());]
			System.out.printf("Vetor B posicao %d: ", cont);
			[vetorB[cont] = Integer.parseInt(System.console().readLine());]
			System.out.printf("Operacao %d: ", cont);
			[op[cont] = System.console().readLine().charAt(0);]
		}
		
		// Processamento
		for(int cont = 0; cont < vetorA.length; cont++) {
			switch(op[cont]) {
				case '+': [resultados[cont] = vetorA[cont] + vetorB[cont];] break;
				case '-': [resultados[cont] = vetorA[cont] ‑ vetorB[cont];] break;
				case '*': [resultados[cont] = vetorA[cont] * vetorB[cont];] break;
				case '/': [resultados[cont] = vetorA[cont] / vetorB[cont];] break;
			}
		}
		
		// Saida
		System.out.println("\n------------ RESULTADOS ------------");
		for(int cont = 0; cont < vetorA.length; cont++) {
			System.out.printf("%d %c %d = %d\n", vetorA[cont], op[cont], vetorB[cont], resultados[cont]);
		}
	}
}

