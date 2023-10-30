# Orienta-o-a-Objetos-Classes-e-m-todos-com-retorno
Anotação da Orientação a Objetos: Classes e métodos com retorno

                                                     Orientação a Objetos: Classes e métodos com retorno



Método com retorno

double obterAutonomia( ){
    return capCombustivel * consumoConbustivel;
}

Como é um método com retorno? existem duas informações extremamente uteis na tela, o void significa que eu não estou retornando nada, nos métodos com retorno
ao invés de utilizar o void nós va,os utilizar o tipo ad informação que aquele método vai retornar e nós podemos ter da mesma forma qualquer lógica de
programação porém no final do método nós temos que utilizara palavra chave return com o valor que a gente quer retornar pro desenvolvedor que vai utilizar
essa classe.

Ex:

package com.madu.poo.classes.e.métodos.com.retorno;

public class Carro {
		
		String marca;
		String modelo;
		int numPassageiros;
		double capCombustivel;
		double consumoCombustivel;
		
		void exibirAutonomia() {
			System.out.println("A autonomia do carro é: " + capCombustivel * consumoCombustivel + " km");
		}
		
		double obterautonomia() {
			
			System.out.println("Método obterAltonomia foi chamado.");
			
			return capCombustivel * consumoCombustivel;
		}
	}


Ex:

package com.madu.poo.classes.e.métodos.com.retorno;

public class TesteCarro {

	public static void main(String[] args) {
		
		Carro van = new Carro();
		van.marca = "Fiat";
		van.modelo = "Ducato";
		van.numPassageiros = 10;
		van.capCombustivel = 100;
		van.consumoCombustivel = 0.2;

		System.out.println(van.marca);
		System.out.println(van.modelo);
		
		van.exibirAutonomia();
		
		double autonomia = van.obterautonomia();
		System.out.println("Altonomia di carro é: " + autonomia);
		System.out.println("Altonomia di carro é: " + van.obterautonomia());
	}

}


Console:
Fiat
Ducato
A autonomia do carro é: 20.0 km
Método obterAltonomia foi chamado.
Altonomia di carro é: 20.0
Método obterAltonomia foi chamado.
Altonomia di carro é: 20.0
