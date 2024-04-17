public class MaquinaCafe {
    int acucarDisponivel;

    void fazerCafe(int qtdAcucar) {
        if(acucarDisponivel >= qtdAcucar) {
            acucarDisponivel -= qtdAcucar;
            System.out.println("Café com " + qtdAcucar + "g de açúcar feito!");
        } else {
            System.out.println("Açúcar insuficiente para fazer o café. Fazendo café sem açúcar.");
        }
    }

    void fazerCafe() {
        fazerCafe(10); // chama o outro método fazerCafe com 10g de açúcar por padrão
    }
}

public class TesteMaquinaCafe {
    public static void main(String[] args) {
        MaquinaCafe maquina = new MaquinaCafe();
        maquina.acucarDisponivel = 100; // atribui a quantidade de açúcar disponível

        maquina.fazerCafe(15); // testa fazer café com 15g de açúcar
        maquina.fazerCafe(); // testa fazer café com a quantidade padrão de açúcar
    }
}
