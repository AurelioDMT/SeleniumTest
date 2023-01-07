tags: #programação/java
status: #zettel/fleeting

# Como Java funciona

- A linguagem Java tem seu grande diferencial, que é, compilando em um dispositivo, ele é capaz de rodar em todos os outros (que tiverem suporte a Java).

- No Java, você escreve o código uma vez e distibruir para vários dispositivos.

>Write Once Run Anywhere \- WORA

- Java é uma **linguagem alto nível**, que a gente pode escrever arquivos ".java". Essa arquivo ".java" é compilado em um arquivo ".class" (arquivo intermediário). Cada dispositivo terá um programa que consegue entender esse arquivo intermediário.
	- O código **.java** passa por um compilador (JavaC);
	- que vira um arquivo intermediário **.class**, trantando-se de um *ByteCode*;
	- logo após, é mandado para uma maquina virtual java (JVM), interpretando o código e, finalmente, rodando na máquina principal.

- Para um sistema rodar um código Java, ele precisa ter um programa instalado, chamado: JRE - Java Runtime Environment %% Usuário final %%
- Para programar em Java, um sistema precisa do JDK - Java Development Kit %% Dev %%

- A linguagem Java utiliza do padrão **CamelCase**.
---
- Versão do JDK utilizada no curso: 14
- IDE utilizada no curso: IntelliJ

# Começando a programar (conceitos básicos)

- Como sempre, começamos printando "Hello world!" na tela:
```Java
public class MeuPrimeiroPrograma {  
    public static void main(String[] args) {  
        System.out.println("Hello world!");  
    }  
}
```

- O método "main", sempre vai ser necessário.
- Tudo em java é feito em blocos, que são representados por chaves "{ }". Logo, não é necessário indentação.
- Toda instrução em java tem que terminar com ";". 

## Declarando variáveis

- Variáveis são espaços de memória alocados.

```Java
public class MeuPrimeiroPrograma {  
    public static void main(String[] args) {  
        var login = "Ola";  
    }  
}
```

- Para declarar variáveis, necessita-se da palavra privada "var".
- Então, definimos uma variável chamada "login", com o conteúdo "Ola"
---
```Java
public class MeuPrimeiroPrograma {  
    public static void main(String[] args) {  
        var login = "Ola";  
        login = "Mundo";  
        System.out.println(login);  
    }  
}
```

- Como já definimos a varíavel, podemos mudar o conteúdo dela a vontade.
- No exemplo, o terminal printou "Mundo".

### Tipos de variáveis
- Texto (Strings)
- Números (Int)
- Números fracionados (Double)
- Boleanas (Verdadeiro | Falso)              

### Tipos de dados
- `String login = "Olá";` - Representação do texto (ASCII).
- `int number1 = 10;` - Representação de números inteiros.
- `double percent = 24.54;` - Representação de números fracionados.
- `boolean isDriver = true;` - Representação booleana (estado verdadeiro ou falso).

## Tipos Primitivos
```Java
public class App {  
    public static void main(String[] args) {  
        boolean isLogged = true; // verdadeiro ou falso  
        byte b = 127; // conjunto de 8 bits = 1 byte  
        char c = 'c'; // caracter  
        String character = "c"; // sequência de caracteres  
        short s = -192; // int (com menos espaços)  
        int i = 234;  
        long l = 321234324324L; // int(longo)  
        float f = 123.4355f; // 32 bit (menor que double)  
        double d = 12.23; // 64 bit  
    }
```

### Tabela (w3schools)

| Data Type | Tamanho | Descrição |
| :-: | :-: | :-: |
| byte | 1 byte | Guarda números inteiros de -128 a 127 |
| short | 2 bytes | Guarda números inteiros de -32.768 a 32.767
| int | 4 bytes | Guarda números inteiros de -2,147,483,648 a 2,147,483,647
| long | 8 bytes | Guarda números inteiros de -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807
| float | 4 bytes | Guarda números fracionados, suficiente para guardar 6 a 7 números decimais
| double | 8 byts | Guarda números fracionados, suficiente para guardar 15 números decimais
| boolean | 1 bit | Guarda verdadeiro ou falso
| char | 2 bytes | Guarda um único caracter/letra ou valores ASCII

## Casting (converter tipos)

- Geralmente essa conversão é feita de um tipo maior pra um menos, ou às vezes, pra transformar um número fracionado em inteiro.
```Java
public class App {  
    public static void main(String[] args) {  
        double dd = 10.23;  
        short ss = 32;  
  
        float x = (float) dd / ss;  
    }  
}
```


## Usando o terminal para compilar e rodar o código

- Como dito antes, o código precisa ser compilado em bytecode, para que a JVM interprete.

- Primeiro você vai dar um `cd` no diretório do seu projeto.
- Logo após, irá compilar com o comando: `javac {nome_do_programa.java}`.
- Em seguida, usará o comando: `java {nome_do_programa}`, e pronto.

## Argumentos

- Na seguinte função:
```Java
public class MeuPrimeiroPrograma {  
    public static void main(String[] args) {  
        System.out.println("Olá, " + args[0]);  
    }  
}
```

- Se rodar assim, sem passar nenhum argumento, vai dar erro.

- Nesse caso, se você for rodar no terminal, ou passar o argumento por outras formas.
	- ex: `java {nome_do_programa} {argumentos}`
- Vai retornar: `Olá {argumentos}`
- Você pode mandar quantos argumentos quiser.

- Então os argumentos da função "main" (`String[] args`), é uma referência à um espaço de memória, onde se encontra alocado, uma coleção de strings.

## Input do usuário (interação do usuário)

- Para dar um input, você precisa importar o módulo "Scanner".
```Java
import java.util.Scanner;  
  
public class Input {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
  
        System.out.print("Digite seu nome: ");  
        String name = scanner.nextLine();  
  
        System.out.println("Olá, " + name);  
    }  
}
```

- Nesse comando irá retornar: `Olá, {nome}`.

## Escopo de variáveis

- A variável só irá funcionar no escopo em que foi declarada.

- Exemplo que **não vai** dar certo:
```Java
public class App {  
    public static void main(String[] args) {  
        if (true){  
            int x = 10;  
        }  
  
        System.out.println(x);  
    }  
}
```
- A variável "x", está somente no escopo do "if", depois ela some. Então, daria um erro no programa, porque não existiria a variável "x".

- Exemplo que **vai** dar certo:
```Java
public class App {  
    public static void main(String[] args) {  
        int x;  
        if (true){  
             x = 10;  
        }  
  
        System.out.println(x);  
    }  
}
```

## Variável imutável (Constantes)

- Uma variável constante, é uma variável que não muda, por exemplo o número PI, que é constante e não muda. Geralmente, essas variáveis são declaradas com letras maiúsculas.
```Java
public class App {  
    public static void main(String[] args) {  
        final double PI = 3.14159;  
    }  
}
```
- Nesse exemplo, a palavra privada "final" é utilizada. Proibindo de você mutar ela.

## Visibilidade (public, private, protected)

- Se não declarada a visibilidade, vai ser padrão, que é, será reconhecida pelas classes que estão no mesmo escopo.

### Public (visibilidade pública)
- Se declarada, pode ser acessada por qualquer classe em qualquer pacote.

### Private (visibilidade privada)
- Se declarada, somente a classe atual pode acessar.

# POO (programação orientada a objetos)
- A classe é simplesmente um **molde** para se criar objetos.

- Uma classe pode definir membros, que são:
	- propriedades (atributos)
	- métodos (comportamentos)

## Getters e Setters
- Basicamente, são métodos para alterar (setter) ou retornar (getter) atributos privados.

`User.java`
```Java
public class User {  
    public String firstName;  
    public String lastName;  
    private String fullName;  
    private int age;  
  
    // setter  
    public void setAge(int age) {  
        this.age = age;  
    }  
  
    // getter  
    public int getAge() {  
        return age;  
    }  
}
```
- Nesse exemplo, o atributo "age" é privado, então eu preciso de um método para setar e para mostrar ele.

`App.java`
```Java
public class App {  
    public static void main(String[] args) {  
        User userA = new User();  
  
        userA.firstName = "Luiz";  
        userA.lastName = "Henrique";  
  
        userA.setAge(21); // Setando idade  
        int age = userA.getAge(); // Atribuindo idade a uma variável  
  
        System.out.println(age); // Mostrando variável  
    }  
}
```

- É recomendado que, você deixe os atributos da classe em privado, para que só haja mudança com métodos. Isso ajuda na integridade do código.

## Arrays
- Arrays são um conjunto, que possui indices.

- Exemplo de um array de objetos.
```Java
public class App {  
    public static void main(String[] args) {  
        User[] users = new User[10];  
  
        for (int i = 0; i < users.length; i++) {  
          User actual = new User();  
          actual.setFirstName("Nome " + i);  
          actual.setlastName("Sobrenome " + i);  
          users[i] = actual; // Armazenar objeto dentro do array  
        }  
  
        System.out.println(users[2].getFirstName());  
        System.out.println(users[2].getLastName());  
    }  
}
```

- Nesse exemplo, colocamos um limite no tamanho do array, agora para não precisarmos colocar esse limite, é preciso criar um objeto do tipo "lista".
```Java
import java.util.ArrayList;  
import java.util.List;  
  
public class App {  
    public static void main(String[] args) {  
        List<User> users = new ArrayList<>();  
  
        int i = 0;  
        while (i < 10) {  
            User actual = new User("nome " + i, "Sobrenome " + i);  
            users.add(actual);  
            i++;  
        }  
  
        System.out.println(users.get(2).getFirstName());  
        System.out.println(users.get(2).getLastName());  
  
        User user11 = new User("Nome 11", "Sobrenome 11");  
        users.add(user11);  
  
        System.out.println(users.get(10).getFirstName());  
        System.out.println(users.get(10).getLastName());  
    }  
}
```

## Construtor
- Um construtor é um método que, pode se dizer, que inicia um objeto.

- Na sintaxe é um método com o mesmo nome da classe.
```Java
public class User {  
    private String firstName;  
    private String lastName;  

	// Construtor
    public User(String firstName, String lastName) {  
        this.firstName = firstName;  
        this.lastName = lastName;  
    }
}
```

- Logo, quando eu for instansiar um objeto, necessariamente preciso passar os atributos compostos anteriormente no construtor.

## Ordenação
- Basicamente, importamos um módulo chamado "Arrays" e utilizamos o método "sort".

```Java
import java.util.Arrays;  
  
public class App {  
    public static void main(String[] args) {  
        int[] numbers = new int[]{3,45,6,3,45,6,8,23,54,6,7,8};  
        Arrays.sort(numbers);  
  
        System.out.println(numbers); // hashcode  
        System.out.println(Arrays.toString(numbers)); // conteúdo  
    }  
}
```

## Comparando arrays
- Para comparar o conteúdo dos arrays, importamos o módulo "Arrays" e utilizamos o método "equals".
```Java
import java.util.Arrays;  
  
public class Main {  
    public static void main(String[] args) {  
        int[] numbersA = new int[]{1, 2, 3};  
        int[] numbersB = new int[]{1, 2, 3};  
  
        System.out.println(numbersA == numbersB); // comparando hashcode  
        System.out.println(numbersA.equals(numbersB));  
  
        System.out.println(numbersA + " " + numbersB); // hashcode diferente  
  
        System.out.println(Arrays.equals(numbersA, numbersB)); // comparando conteúdo  
    }  
}
```

- Saida no terminal:
`false`
`false`
`[I@7530d0a [I@27bc2616`
`true`

## Sobrecarga de métodos
- Você conseguei criar vários métodos com o mesmo nome e com parâmetros diferentes.
```Java
public class User {  
    private String firstName;  
    private String lastName;  
  
    public User(String firstName, String lastName) {  
        this.firstName = firstName;  
        this.lastName = lastName;  
    }  
  
    public void setFirstName (String firstName) {  
        this.firstName = firstName;  
    }  
  
    public String getFirstName () {  
        return firstName;  
    }  
  
    public void setlastName (String lastName) {  
        this.lastName = lastName;  
    }  
  
    public String getLastName () {  
        return lastName;  
    }
      
    public String output() {  
        return firstName.toUpperCase() + " " + lastName.toUpperCase();  
    }
      
    public String output (boolean showLastName) {  
        if (showLastName) {  
            return output();  
        }  
        return firstName;  
    }  
}
```
- Neste caso, se eu chamar a função "output" e não passar nada, irá retornar o nome completo. Caso eu passe o parâmetro booleano, ele irá somente retornar o primeiro nome.
## Hashcode e Equals
- Estes são dois dos métodos que, sempre vão estar em qualquer objeto.
- Declarando eles, a sua classe começa a ser comparada pelo conteúdo (que você especificou), não pelo espaço na memória, ou seja, se você criou duas classes com os mesmos atributos, elas vão dar true pra comparação. == E os números de hash serão os mesmos.
```Java
@Override  
public boolean equals(Object o) {  
    if (this == o) return true;  
    if (o == null || getClass() != o.getClass()) return false;  
    User user = (User) o;  
    return Objects.equals(firstName, user.firstName) && Objects.equals(lastName, user.lastName);  
}  
  
@Override  
public int hashCode() {  
    return Objects.hash(firstName, lastName);  
}
```

## Static
- Basicamente, a palavra privada static, quando colocada em uma variável, ela vai pertencer a classe e não ao objeto que foi referenciado. Por exemplo, na classe:
### Exemplo 1 (sem static)
`User.java`
```Java
public class User {  
    private String firstName;  
    private String lastName;  
  
    private int cont = 0; // não estatico  
  
    public User(String firstName, String lastName) {  
        this.firstName = firstName;  
        this.lastName = lastName;  
    }  

	// setter que vai somando cada vez que é chamado
    public void setCont(int cont) {  
        this.cont = this.cont + cont;  
    }  

	// getter
    public int getCont() {  
        return cont;  
    }
}
```

`Main.java`
```Java
public class Main {  
    public static void main(String[] args) {  
        User luiz = new User("Luiz", "Henrique");  
        User cesar = new User("Cesar", "Henrique");  
  
        luiz.setCont(1);  
        luiz.setCont(1);  
        luiz.setCont(1);  
  
        cesar.setCont(2);  
        cesar.setCont(2);  
        cesar.setCont(2);  
  
        System.out.println(luiz.getCont());  
        System.out.println(cesar.getCont());  
    }  
}
```
- O retorno vai ser:
`3`
`6`

### Exemplo 2 (com static)
`User.java`
```Java
public class User {  
    private String firstName;  
    private String lastName;  
  
    private static int cont = 0; // estatico
  
    public User(String firstName, String lastName) {  
        this.firstName = firstName;  
        this.lastName = lastName;  
    }  

	// setter que vai somando cada vez que é chamado
    public void setCont(int cont) {  
        this.cont = this.cont + cont;  
    }  

	// getter
    public int getCont() {  
        return cont;  
    }
}
```

`Main.java`
```Java
public class Main {  
    public static void main(String[] args) {  
        User luiz = new User("Luiz", "Henrique");  
        User cesar = new User("Cesar", "Henrique");  
  
        luiz.setCont(1);  
        luiz.setCont(1);  
        luiz.setCont(1);  
  
        cesar.setCont(2);  
        cesar.setCont(2);  
        cesar.setCont(2);  
  
        System.out.println(luiz.getCont());  
        System.out.println(cesar.getCont());  
    }  
}
```
- Resultado:
`9`
`9`

### Resumo
- Então, quando declarado static, tanto o user "luiz" e o "cesar" vão ter essa variável compartilhada. 

# Exercicios
## 1. Fazer uma calculadora simples, que rode no terminal.
```Java
	public class Calculate {  
	    public static void main(String[] args) {  
	        int x = Integer.parseInt(args[1]);  
	        int y = Integer.parseInt(args[2]);  
	  
	        if (args[0].equals("somar")) {  
	            sum(x, y);  
	        } else if (args[0].equals("subtrair")) {  
	            minus(x, y);  
	        } else if (args[0].equals("multiplicar")) {  
	            multiply(x, y);  
	        } else if (args[0].equals("dividir")) {  
	            divide(x, y);  
	        } else {  
	            System.out.println("Nenhuma instrução definida");  
	        }  
	    }  
	    
	    static void sum(int x, int y) {  
	        System.out.println(x + y);  
	    }  
	  
	    static void minus(int x, int y) {  
	        System.out.println(x - y);  
	    }  
	  
	    static void multiply(int x, int y) {  
	        System.out.println(x * y);  
	    }  
	  
	    static void divide(int x, int y) {  
	        System.out.println(x / y);  
	    }  
	}
```

## 2. Fazer um gerador de números da mega sena.
- Para fazer um gerador de números, precisamos importar uma biblioteca chamada "Random".

### Com While:
```Java
import java.util.Random;  

public class MegaSena {  
	public static void main(String[] args) {  
		int x;  
		Random generate = new Random();  
  
		int i = 0;  
		while(i < 6) {  
			int number = generate.nextInt(60);  
			System.out.println(number);  
			i++;  
		}  
	}
}
```

### Com For:
```Java
import java.util.Random;  
  
public class MegaSena {  
	public static void main(String[] args) {  
		int x;  
		Random generate = new Random();  
  
		for(int i = 0; i < 6; i++) {  
			int number = generate.nextInt(60);  
			System.out.println(number);  
		}  
	}
}
```

## 3. Fazer a sequência de fibonacci.
```Java
import java.util.Scanner;  
  
public class App {  
	public static void main(String[] args) {  
		Scanner input = new Scanner(System.in);  
		int f1 = 0;  
		int f2 = 1;  
		int limit = input.nextInt();  
  
		while (f2 < limit) {  
			int fn = f1 + f2;  
			if (fn > limit)  
				break;  
			System.out.println(fn);  
			f1 = f2;  
			f2 = fn;  
		}  
	}
}
```

# References
- [CURSO DE JAVA - PROGRAMAÇÃO - Tiago Aguiar](https://www.youtube.com/playlist?list=PLJ0AcghBBWSi6nK2CUkw9ngvwWB1gE8mL)
- https://www.w3schools.com/java/java_data_types.asp