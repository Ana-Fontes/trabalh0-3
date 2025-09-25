package contato;

public class Contato {
    private int codigo;
    private String nome;
    private String endereco;
    private String email; // não pode ser modificado fora da classe
    private String telefone;
    private String observacao;

    // Construtor I: Código
    public Contato(int codigo) {
        if (validarCodigo(codigo)) {
            this.codigo = codigo;
        }
        this.nome = "";
        this.endereco = "";
        this.email = "";
        this.telefone = "";
        this.observacao = "";
    }

    // Construtor II: Código e nome
    public Contato(int codigo, String nome) {
        this(codigo);
        this.nome = nome;
    }

    // Construtor III: Código, nome e e-mail
    public Contato(int codigo, String nome, String email) {
        this(codigo, nome);
        this.email = email != null ? email : "";
    }

    // Construtor IV: Telefone
    public Contato(String telefone) {
        this.codigo = 0;
        this.nome = "";
        this.endereco = "";
        this.email = "";
        if (validarTelefone(telefone)) {
            this.telefone = telefone;
        } else {
            this.telefone = "";
        }
        this.observacao = "";
    }

    // Getters e Setters
    public int getCodigo() {
        return codigo;
    }

    public void setCodigo(int codigo) {
        if (validarCodigo(codigo)) {
            this.codigo = codigo;
        } else {
            System.out.println("Código inválido!");
        }
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getEndereco() {
        return endereco;
    }

    public void setEndereco(String endereco) {
        this.endereco = endereco;
    }

    public String getEmail() { // Somente leitura
        return email;
    }

    public String getTelefone() {
        return telefone;
    }

    public void setTelefone(String telefone) {
        if (validarTelefone(telefone)) {
            this.telefone = telefone;
        } else {
            System.out.println("Telefone inválido!");
        }
    }

    public String getObservacao() {
        return observacao;
    }

    public void setObservacao(String observacao) {
        this.observacao = observacao;
    }

    // Método para imprimir informações do contato
    public void imprimirContato() {
        System.out.println("Código: " + codigo);
        System.out.println("Nome: " + nome);
        System.out.println("Endereço: " + endereco);
        System.out.println("E-mail: " + email);
        System.out.println("Telefone: " + telefone);
        System.out.println("Observação: " + observacao);
        System.out.println("----------------------------");
    }

    // Validador de código
    private boolean validarCodigo(int codigo) {
        return codigo >= 1000 && codigo <= 9999;
    }

    // Validador de telefone
    private boolean validarTelefone(String telefone) {
        return telefone != null && telefone.matches("\\d{8}");
    }

    // Método para duplicar contato
    public Contato duplicar() {
        Contato novo = new Contato(this.codigo);
        novo.setNome(this.nome);
        novo.setEndereco(this.endereco);
        novo.setTelefone(this.telefone);
        novo.setObservacao(this.observacao);
        // email é final, só podemos setar no construtor
        return new Contato(this.codigo, this.nome, this.email);
    }

    // Verificar se contato está totalmente preenchido
    public boolean estaPreenchido() {
        return codigo != 0 &&
               !nome.isEmpty() &&
               !endereco.isEmpty() &&
               !email.isEmpty() &&
               !telefone.isEmpty() &&
               !observacao.isEmpty();
    }
}
