# AVALIA-O-2-TI-AQS
package Valores;

import java.util.ArrayList;
import java.util.List;

public class Valor {
	
	public boolean valor(int num){
		
		
		if( num >= -1 && num < 11) {
		
		return true;
		
		}
		else{
		return false;
		}
	}
	
	public int del(int num){
		
		int i;
		int deletado;
		List<Integer> teste = new ArrayList<Integer>();
        for (i = 10; i > 0; i--) {
            teste.add(i);
        }
        for (i = 10; i > 0; i--) {
        	if (num = teste[i]){
        		deletado = num;
        	}
        }
		
		return deletado;
	}
	
		public double mean(int num){
		
		int i;
		int soma = 0;
		double media;
		List<Integer> teste = new ArrayList<Integer>();
        for (i = 10; i > 0; i--) {
            teste.add(i);
            soma = soma + i;
        }
        media = soma/10;
        
		return media;
	}
		public double greater(int num){
			
			int i;
			int maiorValor = 0;
			List<Integer> teste = new ArrayList<Integer>();
	        for (i = 10; i > 0; i--) {
	            teste.add(i);
	        }
	        for (i = 10; i > 0; i--) {
	        	if (num < teste[i]){
	        		maiorValor = teste[i] ;
	        	}
	        }
	        
			return maiorValor;
		}
		public double lower(int num){
			
			int i;
			int menorValor = 11;
			List<Integer> teste = new ArrayList<Integer>();
	        for (i = 10; i > 0; i--) {
	            teste.add(i);
	        }
	        for (i = 10; i > 0; i--) {
	        	if (num > teste[i]){
	        		menorValor = teste[i] ;
	        	}
	        }
	        
			return menorValor;
		}
	
}


----------------------------

package Teste;

import static org.junit.Assert.*;

import org.junit.Test;

import Valores.Valor;

public class Valores {

	@Test
	public void TesteinserirUmValor() {
		
		Valor v = new Valor();
		boolean resultado = v.valor(11);
		assertEquals(true, resultado);
		
		
	}
	
	@Test
	public void TesteRetornoValorExcluido() {
		
		Valor v = new Valor();
		int resultado = v.del(5);
		assertEquals(5, resultado);
		
		
	}
	@Test
	public void TesteRetornaMedia() {
		
		Valor v = new Valor();
		double resultado = v.mean(8);
		assertEquals(5, resultado,0);
		
		
	}
	@Test
	public void TesteRetornaMairValor() {
		
		Valor v = new Valor();
		double resultado = v.greater(1);
		assertEquals(5, resultado,0);
		
		
	}
	@Test
	public void TesteRetornaMenorValor() {
		
		Valor v = new Valor();
		double resultado = v.lower(1);
		assertEquals(5, resultado,0);
		
		
	}

}
