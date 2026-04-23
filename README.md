# garatuja.ss
Anotações escolares. Sophia E. S. IA25 (2)

  Fazendo uma revisão de html, umas aprendidas a usar main/aside com uma atividade de fazer um site estilo profile/perfil :P
  Aprendendo mais na prática to que na teoria—É melhor fazer do que ficar anotando.
  
# 26/03/2026
  Perdi tudo que eu anotei ontem.

  Prof compartilhou código ent eu vou copiar td disponível p eu n esqueçer.

  # Função x Variável
  
      export {}
    
    // ----------------------------------------------------------------------------
    
    console.log('# Exemplo: função e variavel')
    
    function soma(a: number, b: number) {
      return a + b
    }
    
    let x = soma(20, 30)
    console.log(x)
    
    let y = soma(30, 30)
    console.log(y)
    
    // ----------------------------------------------------------------------------
    
    console.log("# Exemplo: método e atributo");
    
    
    class Z {
      resultado: number = 0
    
      soma(a: number, b: number) {
        this.resultado =  a + b
      }
    
      adicionaUm() {
        this.resultado++
      }  
    }
    
    const z1 = new Z()
    const z2 = new Z()
    
    z1.soma(90, 10)
    z1.adicionaUm()
    
    z2.adicionaUm()
    
    console.log(z1.resultado)
    console.log(z2.resultado)

# Construtores
    
    class TrianguloEquilatero {
      constructor(aste1: number, aste2: number) {
    
      }
    }
    class TrianguloIsosceles {
      constructor(aste1: number, aste2: number, aste3: number) {}
    }
    class TrianguloEscaleno {}
    
    
    class Retangulo {
      altura: number;
      largura: number;
    
      constructor(pAltura: number, pLargura: number) {
        this.largura = pLargura;
        this.altura = pAltura;
      }
    
      calcularArea(): number {
        return this.largura * this.altura;
      }
    }
    
    
    const ret1 = new Retangulo(5, 10);
    const ret2 = new Retangulo(3, 7);
    const ret3 = new Retangulo(8, 4);
    
    console.log(`Área do retângulo 1: ${ret1.calcularArea()}`);
    
    ret1.altura = 10; // Modificando a altura do retângulo 1
    
    console.log(`Área do retângulo 1: ${ret1.calcularArea()}`);
    
    console.log(`Área do retângulo 2: ${ret2.calcularArea()}`);
    console.log(`Área do retângulo 3: ${ret3.calcularArea()}`);

# Sem nome (copiei)
    
    export {}
    
    // ----------------------------------------------------------------------------
    
    class Pessoa {
      nome!: string
      private _anoNasc!: number
    
      gritarNome() {
        console.log(this.nome.toUpperCase() + "!!!")
      }
    
      set anoNasc(ano: number) {
        const now = new Date()
        const anoAtual = now.getFullYear()
        if (ano >= anoAtual) {
          throw "Ano de nascimento não pode ser maior que o ano atual"
        }
        this._anoNasc = ano
      }
    
      get idade() {
        const now = new Date()
        const anoAtual = now.getFullYear()
        return anoAtual - this._anoNasc
      }
    }
    
    const p1 = new Pessoa()
    p1.nome = 'Maria'
    p1.anoNasc = 1990
    
    
    const p2 = new Pessoa()
    p2.nome = 'João'
    p2.anoNasc = 1985
    
    console.log(p1.anoNasc);
    console.log(p2.anoNasc);

# Identificação de Triângulos

    class Triangulo {
      lado1: number;
      lado2: number;
      lado3: number;
    
      constructor(pLado1: number, pLado2: number, pLado3: number) {
        if (
          (pLado1 <= 0 || pLado2 <= 0 || pLado3 <= 0)
          // || (escreva aqui a lógica para verificar se os lados formam um triângulo válido, 
          //   ou seja, a soma de dois lados deve ser maior que o terceiro lado)
        ) {
          throw new Error("O valores não formam um triângulo válido");
        }
        this.lado1 = pLado1;
        this.lado2 = pLado2;
        this.lado3 = pLado3;
      }
    
      get tipo(): string {
        if (this.lado1 === this.lado2 && this.lado2 === this.lado3) {
          return "equilátero";
        }
    
        if (this.lado1 === this.lado2 || this.lado2 === this.lado3 || this.lado1 === this.lado3) {
          return "isósceles";
        }
    
        return "escaleno";
      }
    
      get perimetro(): number {
        return (this.lado1 + this.lado2 + this.lado3) / 2;
      }
    
      get area(): number {
        const p = this.perimetro;
        const a = this.lado1;
        const b = this.lado2;
        const c = this.lado3;
        const area = Math.sqrt(p * (p - a) * (p - b) * (p - c));
        return area;
      }
    }
    
    const equilatero = new Triangulo(10, 10, 10);
    const isosceles = new Triangulo(10, 10, 5);
    const escaleno = new Triangulo(10, 5, 3);
    
    console.log(equilatero.tipo, equilatero.area);

# To-do List
  Nn consegui atualizar (internet n funciona)
  
    export {}

    // ----------------------------------------------------------------------------
    
    class Item {
      title: string = "undefined";
      done: boolean = false;
      constructor(title: string) {
        this.title = title;
      }
    }
    
    class List {
      items: Array<Item> = [];
    
      constructor(filePath: string) {}
      
      // add(item: Item): void {}
      // remove(item: Item): void {}
      // findOneByTitle(title: string): Item | null {}
      // findManyByTitle(title: string): Item[] {}
      // listAll(): Item[] {}
      // saveToFile(filePath: string): void {}
    
      private loadFromFile(filePath: string): void {
        const file = Bun.file(filePath);
    
      }
    }


 # Perguntas
  -> Não tenho mas tenho q fingir q tenho
    Static (mais info sobre; foi falado por pouco tempo)
    Throw (nao entendi o motivo que seria usado)
