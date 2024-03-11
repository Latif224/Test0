# Test0
package Exo1;

import java.util.Arrays;
import java.util.List;
import java.util.Optional;
import java.util.stream.Collectors;

public class MainExo1 {
    public static void main(String[] args) {
        List<Integer> nombres = Arrays.asList(17, 22, 53, 44, 12, 6, 9, 11, 98, 2);
        // 1- Récupérer la liste des nombres pairsl
        List<Integer> nombresPairs = nombres.stream()
                .filter(n -> n % 2 == 0)
                .collect(Collectors.toList());
        System.out.println("Liste des nombres pairs : " + nombresPairs);
        // 2- Récupérer la liste des nombres inférieurs à 44
        List<Integer> nombresInferieursA44 = nombres.stream()
                .filter(n -> n < 44)
                .collect(Collectors.toList());
        System.out.println("Liste des nombres inférieurs à 44 : " + nombresInferieursA44);
        // 3- Le produit de tous les nombres
        Optional<Integer> produit = nombres.stream()
                .reduce((a, b) -> a * b);
        System.out.println("Le produit de tous les nombres : " + produit.orElse(0));
        // 4- Le plus petit nombre
        Optional<Integer> plusPetit = nombres.stream()
                .min(Integer::compareTo);
        System.out.println("Le plus petit nombre : " + plusPetit.orElse(0));
    }
}

