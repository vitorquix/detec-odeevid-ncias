import java.util.ArrayList;
import java.util.HashMap;
import java.util.Random;

import javax.swing.plaf.synth.SynthViewportUI;

public class Principal {

	public static void main(String[] args) {

		Random numbers = new Random();
		int[] variavel = { 2, 5, 3, 2, 2, 2, 5, 3, 6, 2, 5, 3, 5, 2, 2, 7, 2, 5, 3, 2, 9 };
		HashMap<Integer, Integer> evidencias = new HashMap();
		ArrayList<Integer> valores = new ArrayList();

		// INSERE TODOS OS ALERTAS EM UM ARRAY
		  for (int i = 0; i < 50; i++) {
		//for (int i = 0; i < variavel.length; i++) {
			 valores.add(numbers.nextInt(5));
			//valores.add(variavel[i]);
		}

		int target = 3;
		int a = 0;
		int b = 0;
		int iguais = 0;
		int diferentes = 0;

		System.out.println("-------Exemplo: Alerta 3 é Indisponibilidade-------------------------");

		for (int i = 0; i < valores.size(); i++) {
			if (valores.get(i) != 3) {
				System.out.println(i + "º Alerta " + valores.get(i));
			}
			if (valores.get(i).equals(3)) {
				System.out.println(i + "º Indisponibilidade " + valores.get(i));
			}
			if (valores.get(i) == target && i > 3) {
				for (int j = (i + 1); j < (valores.size() - 2); j++) {
					if (valores.get(i - 2) == valores.get(j) && valores.get(i - 1) == valores.get(j + 1)
							&& valores.get(i) == valores.get(j + 2)) {
						b++;
						System.out.println("Evidência da Indisponibilidade: " + valores.get(i - 2));
						System.out.println("Evidência da Indisponibilidade: " + valores.get(i - 1));
						evidencias.put(a++, valores.get(i - 2));
						evidencias.put(a++, valores.get(i - 1));
						break;

					}
				}
			}
		}

		for (int i = 0; i < evidencias.size(); i++) {
			if (evidencias.size() >= 4 && evidencias.get(i) == evidencias.get(i + 2)
					&& evidencias.get(i + 1) == evidencias.get(i + 3)) {
				iguais += 1;
				break;
			} else if (evidencias.size() >= 4) {
				diferentes += 1;
			}

		}

		System.out.println("----------------------------------------------");
		System.out.println("Evidências repetidas pelo menos 1x: " + b);
		System.out.println("Evidencias iguais:" + iguais);
		if (diferentes > 4) {
			System.out.println("Evidencias diferentes:" + "Sim, " + diferentes / 2);
		} else {
			System.out.println("Evidencias diferentes:" + "Nao, " + diferentes / 2);
		}
		// System.out.println("Evidencias diferentes:" + diferentes/2);

	}

}
