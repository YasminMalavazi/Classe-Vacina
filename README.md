import java.util.Arrays;
import java.util.List;

public class Vacina {
    private int id;
    private String nome;
    private String descricao;
    private Integer limiteIdadeMeses; // Limite de idade em meses (pode ser nulo)
    private List<PublicoAlvo> publicoAlvo;

    // Enumeração para o público-alvo
    public enum PublicoAlvo {
        CRIANCA, ADOLESCENTE, ADULTO, GESTANTE
    }

    // Construtor
    public Vacina(int id, String nome, String descricao, Integer limiteIdadeMeses, List<PublicoAlvo> publicoAlvo) {
        this.id = id;
        this.nome = nome;
        this.descricao = descricao;
        this.limiteIdadeMeses = limiteIdadeMeses;
        this.publicoAlvo = publicoAlvo;
    }

    // Getters e Setters
    public int getId() {
        return id;
    }

    public String getNome() {
        return nome;
    }

    public String getDescricao() {
        return descricao;
    }

    public Integer getLimiteIdadeMeses() {
        return limiteIdadeMeses;
    }

    public List<PublicoAlvo> getPublicoAlvo() {
        return publicoAlvo;
    }

    @Override
    public String toString() {
        return "Vacina{" +
                "id=" + id +
                ", nome='" + nome + '\'' +
                ", descricao='" + descricao + '\'' +
                ", limiteIdadeMeses=" + limiteIdadeMeses +
                ", publicoAlvo=" + publicoAlvo +
                '}';
    }

    // Método main para demonstrar o uso da classe Vacina
    public static void main(String[] args) {
        // Criando as vacinas conforme o script SQL
        List<Vacina> vacinas = Arrays.asList(
            new Vacina(1, "BCG", "Proteção contra formas graves de tuberculose (meníngea e miliar)", 60, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(2, "Hepatite B", "Proteção contra o vírus da Hepatite B", null, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(3, "Poliomielite 1, 2 e 3", "Proteção contra o vírus da Poliomielite", null, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(4, "Rotavírus", "Proteção contra o rotavírus humano G1P[8] (ROTA)", 9, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(5, "Pentavalente (DTP, HB, Hib)", "Proteção contra DTP (difteria, tétano, coqueluche), HB (hepatite b) e Hib (influenza tipo b)", 84, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(6, "Pneumocócica 10", "Proteção contra Pneumonias, Meningites, Otites e Sinusites pelos sorotipos que compõem a vacina", 60, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(7, "Meningocócica C", "Proteção contra Meningite meningocócica tipo C", 60, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(8, "COVID-19", "Proteção contra o vírus SARS-CoV-2", 60, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(9, "Febre Amarela", "Proteção contra o vírus da febre amarela", null, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(10, "Tríplice Viral", "Proteção contra os vírus: sarampo, caxumba e rubéola", 72, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(11, "Tetraviral", "Proteção contra os vírus: sarampo, caxumba, rubéola e varicela", 84, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(12, "Hepatite A", "Proteção contra o vírus da Hepatite A", 60, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(13, "DTP", "Proteção contra Difteria, Tétano e Pertussis", 84, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(14, "HPV4", "Proteção contra o Papilomavírus Humano 6, 11, 16 e 18", 180, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(15, "Pneumocócica 23", "Proteção contra Meningites bacterianas, Pneumonias, Sinusite e outros", null, Arrays.asList(PublicoAlvo.CRIANCA)),
            new Vacina(16, "Varicela", "Proteção contra o vírus da varicela (catapora)", 156, Arrays.asList(PublicoAlvo.CRIANCA))
        );

        // Exibindo informações de todas as vacinas
        for (Vacina vacina : vacinas) {
            System.out.println("Informações da Vacina:");
            System.out.println("ID: " + vacina.getId());
            System.out.println("Nome: " + vacina.getNome());
            System.out.println("Descrição: " + vacina.getDescricao());
            System.out.println("Limite de Idade (meses): " + (vacina.getLimiteIdadeMeses() != null ? vacina.getLimiteIdadeMeses() : "Sem limite"));
            System.out.println("Público-Alvo: " + vacina.getPublicoAlvo());
            System.out.println();
        }
    }
}


