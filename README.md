# Avaliação Técnica S2ITf

#### Respostas dos exercicios de múltipla escolha 

Questão 1)

    Resposta Correta: Opção A
-------------------------------------
Questão 2)

    Resposta Correta: Opção D
--------------------------------------
Questão 3)

    Resposta Correta: Opção C
--------------------------------------
Questão 4)

    Resposta Correta: Opção A 
--------------------------------------
Questão 5)

    Resposta Correta: Opção A 
--------------------------------------
Questão 6)

    Resposta Correta: Opção C
--------------------------------------
Questão 7)

    Resposta Correta: Opção E
--------------------------------------

#### Respostas dos exercicios de elaboração de algoritmos  

Questão 8)

```
public int calcula(Integer valorA, Integer valorB) {
	String valorC = "";
    char[] arrayA = valorA.toString().toCharArray();
    char[] arrayB = valorB.toString().toCharArray();
    int maiorIndex = arrayA.length > arrayB.length ? arrayA.length : arrayB.length;
    
    for (int x = 0; x < maiorIndex; x++) {
        if (arrayA.length > x) {
        	valorC += String.valueOf(arrayA[x]);
        }
        if (arrayB.length > x) {
        	valorC += String.valueOf(arrayB[x]);
        }
    }
    Integer c = Integer.valueOf(valorC);
    
    return c > 1000000 ? -1 : c;
}
```
    
--------------------------------------

Questão 9)

```
public class BinaryTree {

	    private int valor;

	    private BinaryTree esquerda;

	    private BinaryTree direita;

		public int getValor() {
			return valor;
		}

		public void setValor(int valor) {
			this.valor = valor;
		}

		public BinaryTree getEsquerda() {
			return esquerda;
		}

		public void setEsquerda(BinaryTree esquerda) {
			this.esquerda = esquerda;
		}

		public BinaryTree getDireita() {
			return direita;
		}

		public void setDireita(BinaryTree direita) {
			this.direita = direita;
		}

	}
	
	public class Calcula {

	    private BinaryTree binaryTree;

	    public Calcula(BinaryTree binaryTree) {
	    	
	        this.binaryTree = binaryTree;
	    }

	    public int somar() {
	        return somar(binaryTree);
	    }

	    private int somar(BinaryTree binaryTree) {

	        if (binaryTree == null) {
	            return 0;
	        }

	        return binaryTree.getValor() + somar(binaryTree.getEsquerda()) + somar(binaryTree.getDireita());
	    }
	}
```
