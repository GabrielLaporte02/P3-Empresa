# P3-Empresa

 controlador de pacote ;
importar  java . útil . Lista Vinculada ;
importar  java . útil . Scanner ;
 controlador de importação . Empresa ;
 Classe  pública Menus {
    public  static  LinkedList < Cliente > clientes = new  LinkedList < Cliente >();
    public  static  LinkedList < Empresa > empresas = new  LinkedList < Empresa >();
  public  static  void  menuPrincipal () lança  IllegalAccessException {

    Scanner  in = new  Scanner ( System . in );
        int  op , cl , opC , opCA , opADC , opE , opADE ;
        Sistema . fora . println ( "___ ___ _____ __ __ __ __" );
        Sistema . fora . println ( "||| ||| || || || || ||" );
        Sistema . fora . println ( "|||\\/||| ||--- ||\\\\|| || ||" );
        Sistema . fora . println ( "||| ||| ||___ || \\\\| ||_||" );
        Sistema . fora . println ( "" );
        fazer {
            menuInicial ();
            op = em . nextInt ();
@@ -21,7 +26,7 @@ public static void menuPrincipal() lança IllegalAccessException{
                    if ( cl == 1 ) {
                        boolean  tfc = loginCliente ();
                        if ( tfc == true ) { // Cliente entrou na conta
                            /* aqui estão todas as opções do cliente */
                            /* aqui estarÃ£o todas as opÃ§Ãµes do cliente */
                            fazer {
                                opçãoCliente ();
                                opC = em . nextInt ();
@@ -30,7 +35,7 @@ public static void menuPrincipal() lança IllegalAccessException{
                                } senão  if ( opC == 2 ) {
                                    //Compra fichas
                                } senão  if ( opC == 3 ) {
                                    // Criar um menu novo com as opções relaciondas a amigos dentro do cliente
                                    // Criar um menu novo com as opções relaciondas a amigos dentro do cliente
                                    fazer {
                                        menuClienteAmigo ();
                                        opCA = em . nextInt ();
@@ -44,23 +49,21 @@ public static void menuPrincipal() lança IllegalAccessException{
                                    } while ( opCA != 0 );
                                } senão  if ( opC == 4 ) {
                                    // Altera dados
                                    fazer {
                                        menuAlterarDadosCliente ();
                                        opADC = em . nextInt ();
                                        if ( opADC == 1 ) {
                                            // altera o nome
                                        } senão  if ( opADC == 2 ) {
                                            // altera o genero
                                        } senão  if ( opADC == 3 ) {
                                            // altera telefone
                                        } else  if ( opADC == 4 ) {
                                            // altera cpf
                                        }
                                    } while ( opADC != 0 );
                                	int  cc ;
                                	fazer {
                                		menuAlterarDadosCliente ();
                                		Sistema . fora . println ( "Deseja alterar mais dados?" );
                                		Sistema . fora . println ( "[1] para sim, [0] para nao: " );
                                		cc = em . nextInt ();
                                		while ( dc != 0 && dc != 1 ) {
                                			Sistema . fora . println ( "Opção inválida... digite novamente: " );
                                			cc = em . nextInt ();
                                		}
                                	} while ( dc != 0 );
                                }
                            } while ( opC != 0 );
                        }
                    } else  if ( cl == 2 ) { // Opção de cadastrar
                    } else  if ( cl == 2 ) { // opções de cadastro
                        cadastroCliente ();
                    } senão {
                        Sistema . fora . println ( "Opção inválida..." );
@@ -75,7 +78,7 @@ public static void menuPrincipal() lança IllegalAccessException{
                    if ( cl == 1 ) {
                        boolean  tfe = loginEmpresa ();
                        if ( tfe == true ) { // Empresa entrou na conta
                            /* aqui estarão todas as ações da empresa */
                            /* aqui estarao todas as acoes da empresa */
                            fazer {
                            opcaoEmpresa ();
                            opE = em . nextInt ();
@@ -102,7 +105,7 @@ public static void menuPrincipal() lança IllegalAccessException{
                            }        
                            } while ( opE != 0 );
                        }
                    } else  if ( cl == 2 ) { // Opção de cadastrar
                    } else  if ( cl == 2 ) { // Opções de cadastro
                        cadastroEmpresa ();
                    } senão {
                        Sistema . fora . println ( "Opção inválida..." );
@@ -144,12 +147,73 @@ public static void menuClienteAmigo() {
    }

  public  static  void  menuAlterarDadosCliente () {
        Sistema . fora . println ( "Menu" );
        Sistema . fora . println ( "[1] para alterar seu nome" );
        Sistema . fora . println ( "[2] para alterar seu genero" );
        Sistema . fora . println ( "[3] para alterar seu telefone" );
        Sistema . fora . println ( "[4] para alterar seu cpf" );
        Sistema . fora . println ( "[0] para Voltar!" );
	  	Scanner  in = new  Scanner ( System . in );
	  	int  opADC ;
	  	Sistema . fora . println ( "Digite os dados abaixo para alteração de dados do perfil" );
    	Sistema . fora . print ( "Nome: " );
    	String  nome = em . próximo ();
    	Sistema . fora . print ( "Senha: " );
    	String  senha = em . próximo ();
    	Sistema . fora . println ( "" );
    	boolean  vf = buscaLoginCliente ( nome , senha );
    	if ( vf == verdadeiro ){
        	for ( int  i = 0 ; i < clientes . size (); i ++) {
                Cliente  aux = clientes . obter ( i );
                if ( aux . getNome (). equalsIgnoreCase ( nome ) && aux . getSenha (). equals ( senha )) {
                	Sistema . fora . println ( "Opções: " );
                    Sistema . fora . println ( "[1] para alterar seu nome" );
                    Sistema . fora . println ( "[2] para alterar seu genero" );
                    Sistema . fora . println ( "[3] para alterar seu telefone" );
                    Sistema . fora . println ( "[4] para alterar seu cpf" );
                    Sistema . fora . println ( "[0] para Voltar!" );
                    Sistema . fora . print ( "Digital: " );
                    opADC = em . nextInt ();
                    if ( opADC == 1 ) {
                        // altera o nome
                    	Sistema . fora . print ( "Digite seu novo nome: " );
                    	String  newNome = in . próximo ();
                    	auxiliar . setNome ( novoNome );
                    } senão  if ( opADC == 2 ) {
                        // altera o genero
                    	Sistema . fora . print ( "Digite seu novo gênero: " );
                    	String  newGen = em . próximo ();
                    	auxiliar . setGenero ( newGen );
                    } senão  if ( opADC == 3 ) {
                        // altera telefone
                    	Sistema . fora . print ( "Digite apenas o DDD: " );
                    	String  ddd = em . próximo ();
                    	while ( ddd . comprimento ()< 2 || ddd . comprimento ()> 3 ) {
                    		Sistema . fora . print ( "DDD inválido digite novamente: " );
                    		dd = em . próximo ();
                    	}
                    	Sistema . fora . print ( "Digite o seu numero de celular: " );
                    	String  num = em . próximo ();
                    	while ( num . comprimento ()< 8 || num . comprimento ()> 10 ) {
                    		Sistema . fora . print ( "Número inválido digite novamente: " );
                    		dd = em . próximo ();
                    	}
                    	String  newNum = "(" + ddd + ")" + num ;
                    	auxiliar . setTelefone ( newNum );
                    } else  if ( opADC == 4 ) {
                        // altera cpf
                    	Sistema . fora . print ( "Digite seu novo CPF: " );
                    	String  novoCPF = em . próximo ();
                    	while ( newCPF . length () != 11 ) { // CPF tem que ter 11 dígitos
                            Sistema . fora . print ( "CPF incorreto, digite novamente (apenas números): " );
                            novoCPF = em . próximo ();
                        }
                    	auxiliar . setGenero ( novoCPF );
                    }
                    senão {
                    	opADC = 0 ;
                    }
                }
            }
    	} senão {
        	Sistema . fora . println ( "Nome ou senhas incorretas... Tente novamente." );
        	Sistema . fora . println ( "" );
        	opADC = 0 ;
        }
    }

  public  static  void  opcaoEmpresa (){
@@ -172,7 +236,7 @@ public static void opcaoCliente() {
        Sistema . fora . println ( "Menu" );
        Sistema . fora . println ( "[1] para ver os produtos" );
        Sistema . fora . println ( "[2] para comprar Tokens" );
        Sistema . fora . println ( "[3] para amigos" ); // cria um novo menu para as opções relacionadas aos amigos
        Sistema . fora . println ( "[3] para amigos" ); // cria um novo menu para as opções relacionadas aos amigos
        Sistema . fora . println ( "[4] para alterar seus dados" );
        Sistema . fora . println ( "[0] para Sair!" );
        Sistema . fora . print ( "Digital:" );
@@ -190,7 +254,7 @@ public static boolean loginCliente() {
            retorno = buscaLoginCliente ( nome , senha );
            if ( retorno == false ) { // Aqui ele da a escolha para tentar fazer login novamente
                Sistema . fora . println ( "Login inválido... Deseja tentar novo?" );
                Sistema . fora . println ( "Digite [1] para sim,[2] para nao : " );
                Sistema . fora . println ( "Digite [1] para sim,[2] para nao : " );
                int  a = em . nextInt ();
                if ( a == 2 ){
                    quebrar ;
@@ -207,15 +271,23 @@ public static void cadastroCliente() {

        Sistema . fora . print ( "Informe seu CPF (apenas números): " );
        String  cpf = em . próximo ();
        while ( cpf . length () != 11 ) { // CPF tem que ter 11 dígitos
            Sistema . fora . print ( "CPF incorreto, digite novamente (apenas números , 11 números ): " );
        while ( cpf . length () != 11 ) { // CPF tem que ter 11 dígitos
            Sistema . fora . print ( "CPF incorreto, digite novamente (apenas números): " ); //CPF 11 DÍGITOS PARA TESTE
            cpf = em . próximo ();
        }

        Sistema . fora . print ( "Informe seu DDD: " );
        String  ddd = em . próximo ();
        Sistema . fora . println ( "Informe seu numero de telefone: " );
        while ( ddd . comprimento ()< 2 || ddd . comprimento ()> 3 ) {
    		Sistema . fora . print ( "DDD inválido digite novamente: " );
    		dd = em . próximo ();
    	}
        Sistema . fora . print ( "Informe seu numero de telefone: " );
        String  numc = em . próximo ();
        while ( numc . comprimento () < 8 || numc . comprimento ()> 10 ) {
    		Sistema . fora . print ( "Número inválido digite novamente: " );
    		numc = em . próximo ();
    	}
        String  telefone = "(" + ddd + ")" + numc ;

        Sistema . fora . print ( "Informe seu genero: " );
@@ -226,17 +298,23 @@ public static void cadastroCliente() {

        Sistema . fora . print ( "Informe uma senha:" );
        String  senha = em . próximo ();

        boolean  cd = verificarCD ( cpf , senha ); // verificando se já existe conta usando esse cpf ou senha

        Sistema . fora . print ( "Informe a quantidade que deseja depositar para compras no App: " );
        int  token = em . nextInt ();

        boolean  cd = verificarCD ( cpf , senha ); // verificando se já existe conta usando esse cpf ou senha
        if ( cd == falso ) {
            Cliente  cliente = novo  Cliente ( código , nome , genero , telefone , cpf , senha ); // Criou novo cliente
            Cliente  cliente = novo  Cliente ( código , nome , genero , telefone , cpf , token , senha ); // Criou novo cliente
            clientes . adicionar ( cliente ); // adicionou novo cliente a lista
            Sistema . fora . println ( "Conta criada com sucesso! Seja bem-vindo" + nome );
            Sistema . fora . println ( "" );
        } senão {
            Sistema . fora . println ( "CPF ou Senha já existente. Conta não criada..." );
            Sistema . fora . println ( "CPF ou Senha já existente. Conta não criada..." );
            Sistema . fora . println ( "" );
        }
    }
  public  static  boolean  buscaLoginCliente ( String  nome , String  senha ) {

public  static  boolean  buscaLoginCliente ( String  nome , String  senha ) {
        // Método para buscar na lista de clientes para fazer login
        for ( int  i = 0 ; i < clientes . size (); i ++) {
            Cliente  aux = clientes . obter ( i );
@@ -247,7 +325,8 @@ public static boolean buscaLoginCliente(String nome, String senha) {
        retornar  falso ;
    }

  public  static  boolean  verificarCD ( String  cpf , String  senha ) {
public  static  boolean  verificarCD ( String  cpf , String  senha ) {

        // Metodo para buscar cliente ja existente
        for ( int  i = 0 ; i < clientes . size (); i ++) {
            Cliente  aux = clientes . obter ( i );
@@ -257,7 +336,8 @@ public static boolean checkCD(String cpf, String senha) {
        }
        retornar  falso ;
    }
    public  static  void  cadastroProduto (){

public  static  void  cadastroProduto (){

        Scanner  in = new  Scanner ( System . in );
        Sistema . fora . print ( "Informe o nome do produto que deseja vender: " );
@@ -277,7 +357,7 @@ public static void cadastroProduto(){

    }

    public  static  boolean  loginEmpresa () {
public  static  boolean  loginEmpresa () {
          Scanner  in = new  Scanner ( System . in );
          boolean  retorno ;
          fazer {
@@ -288,8 +368,8 @@ public static boolean loginEmpresa() {
              String  senha = em . próximo ();
              retorno = buscaLoginEmpresa ( cnpj , senha );
              if ( retorno == false ) { // Aqui ele da a escolha para tentar fazer login novamente
                  Sistema . fora . println ( "Login inválido ... Deseja tentar novo?" );
                  Sistema . fora . println ( "Digite [1] para sim,[2] para nao : " );
                  Sistema . fora . println ( "Login inválido ... Deseja tentar de novo?" );
                  Sistema . fora . println ( "Digite [1] para sim,[2] para nao : " );
                  int  a = em . nextInt ();
                  if ( a == 2 ){
                      quebrar ;
@@ -305,10 +385,10 @@ public static void cadastroEmpresa() {
          Sistema . fora . print ( "Informe o nome da empresa: " );
          String  nome = em . próximo ();

          Sistema . fora . print ( "Informe o CNPJ da empresa (apenas números ): " );
          Sistema . fora . print ( "Informe o CNPJ da empresa (apenas números ): " );
          String  cnpj = em . próximo ();
          while ( cnpj . length () != 14 ) { // CNPJ tem que ter 14 dígitos
              Sistema . fora . print ( "CNPJ incorreto, digite novamente ( apenas números , 14 números): " );
          while ( cnpj . length () != 14 ) { // CNPJ tem que ter 14 dígitos
              Sistema . fora . print ( "CNPJ incorreto, digite novamente (apenas números , 14 números): " );
              cnpj = em . próximo ();
          }

          Sistema . fora . print ( "Informe o DDD: " );
          String  ddd = em . próximo ();
          Sistema . fora . println ( "Informe o numero de telefone: " );
          String  numc = em . próximo ();
          String  telefone = "(" + ddd + ")" + numc ;
  
          Sistema . fora . print ( "Informe o saldo da empresa: " );
           saldo duplo = em . próximoDouble ();
  
          Sistema . fora . print ( "Informe uma senha:" );
          String  senha = em . próximo ();
  
          Empresa  empresa = new  Empresa ( nome , telefone , cnpj , saldo , senha ); // Criou nova empresa
          empresas . adicionar ( empresa ); // Adiciona a lista de empresas
          Sistema . fora . println ( "Empresa cadastrada com sucesso!" );
      }
  
     public  static  boolean  buscaLoginEmpresa ( String  cnpj , String  senha ) {
          /*
           * Método para buscar na lista de empresa para fazer login
           * (Apenas ter uma empresa criada a lista facilita)
           */
          for ( int  i = 0 ; i < empresas . size (); i ++) {
              Empresa  aux = empresas . obter ( i );
              if ( aux . getCnpj () . ​​equals ( cnpj ) && aux . getSenha () . equals ( senha )) {
                  retorna  verdadeiro ;
              }
          }
          retorna  verdadeiro ;
      }
}
