# Classe Genérica para conexão com PostgreSql e MySql

## Classe Genérica para conexão com PostgreSql e MySql, para facilitar o uso de vários bancos de dados.



[Artigos](https://www.devmedia.com.br/artigos/)[Java](https://www.devmedia.com.br/artigos/java)Classe Genérica para conexão com PostgreSql e MySql

Este post apresenta uma classe Java genérica para conexão com os bancos de dados MySQL e PostgreSQL.

```
package br.com.dragon.util.conexao;
import java.sql.*;
/**
*
* @author mayron
*/
public class Conexao {
	private String local;
	private String user;
	private String senha;
	private Connection c;
	private Statement statment;
	private String str_conexao;
	private String driverjdbc;

	public Conexao(String bd, String local, String porta,
	String banco, String user, String senha) {
		if (bd.equals("PostgreSql")){
  			setStr_conexao("jdbc:postgresql://"+ local +":" + porta +"/"+ banco);
  			setLocal(local);
  			setSenha(senha);
  			setUser(user);
  			setDriverjdbc("org.postgresql.Driver");
  		 }else {
  			if (bd.equals("MySql")) {
     				setStr_conexao("jdbc:mysql://"+ local +":" + porta +"/"+ banco);
     				setLocal(local);
     				setSenha(senha);
     				setUser(user);
     				setDriverjdbc("com.mysql.jdbc.Driver");
 			}
		}
  	}

	public void configUser(String user, String senha) {
		setUser(user);
		setSenha(senha);
	}

	public void configLocal(String banco) {
		setLocal(banco);
	}

	//Conexão com o Banco de Dados
	public void conect(){
		try {
			Class.forName(getDriverjdbc());
			setC(DriverManager.getConnection(getStr_conexao(), getUser(), getSenha()));
			setStatment(getC().createStatement());
		}catch (Exception e) {
			System.err.println(e);
			e.printStackTrace();
		}
	}

	public void disconect(){
		try {
			getC().close();
		}catch (SQLException ex) {
			System.err.println(ex);
			ex.printStackTrace();
		}
	}

	public ResultSet query(String query){
		try {
			return getStatment().executeQuery(query);
		}catch (SQLException ex) {
			ex.printStackTrace();
			return null;
		}
	}

	// GETs AND SETs
	public String getLocal() {
		return local;
	}

	public void setLocal(String local) {
		this.local = local;
	}

	public String getUser() {
		return user;
	}

	public void setUser(String user) {
		this.user = user;
	}

	public String getSenha() {
		return senha;
	}

	public void setSenha(String senha) {
		this.senha = senha;
	}

	public Connection getC() {
		return c;
	}

	public void setC(Connection c) {
		this.c = c;
	}

	public Statement getStatment() {
		return statment;
	}

	public void setStatment(Statement statment) {
		this.statment = statment;
	}

	public String getStr_conexao() {
		return str_conexao;
	}

	public void setStr_conexao(String str_conexao) {
		this.str_conexao = str_conexao;
	}

	public String getDriverjdbc() {
		return driverjdbc;
	}

	public void setDriverjdbc(String driverjdbc) {
		this.driverjdbc = driverjdbc;
	}

}
```

**Listagem 1**. Classe de conexão genérica

Para utilizá-la, seguimos a seguinte sintaxe:

```
Conexao("BANCO","LOCAL/IP","PORTA","MEU DB","USUARIO","SENHA");
```

**Listagem 2**. Sintaxe para uso da classe Conexao

Para selecionar o banco, no primeiro parâmetro informe:

- "MySql"
- "PostgreSql"

**Nota**: digite da mesma forma apresentada a cima.

```
Conexao c = new Conexao("PostgreSql","localhost","5432","db1","us","123");
c.conect();
//...
c.disconect();
```

**Listagem 3**. Exemplo de uso

Ainda tem muito a se melhorar, mas já é meio caminho andado.

Os drivers JDBC estão disponíveis pra download aqui nessa dica.

Tecnologias:

- [Java](https://www.devmedia.com.br/java/)
- JDBC
- [MySQL](https://www.devmedia.com.br/mysql/)
- [PostgreSQL](https://www.devmedia.com.br/postgresql/)
- [SQL](https://www.devmedia.com.br/sql/)