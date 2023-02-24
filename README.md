# Calcula a médiae diz se foi aprovado ou não

## Classe que recebe as notas, retorna a média e diz se foi aprovado ou não
````
package br.com.principal;

import javax.swing.JOptionPane;

import br.com.calculo.bo.Calculo;
	
public class Principal {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		double nota1, nota2, nota3,media;
		
		JOptionPane.showMessageDialog(null, "Digite suas três notas para que a média seja calculada.");
		
		nota1 = Double.parseDouble(JOptionPane.showInputDialog("Primeira nota:"));
		nota2 = Double.parseDouble(JOptionPane.showInputDialog("Segunda nota:"));
		nota3 = Double.parseDouble(JOptionPane.showInputDialog("Terceira nota:"));

		Calculo m = new Calculo();
		
		media = m.media(nota1, nota2, nota3);
		
		if (media >= 7.0) {
	        JOptionPane.showMessageDialog(null,"Média: " + media + ", você foi aprovado.");
	    } else {
	        JOptionPane.showMessageDialog(null,"Média: " + media + ", você foi reprovado.");
	    }
		System.exit(0);
		}
}
````

## Classe que calcula a média
````
package br.com.calculo.bo;

public class Calculo {
	
	public double media(double n1, double n2, double n3) {
		return (n1+n2+n3)/3;
	}

}
````


