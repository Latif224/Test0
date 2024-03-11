# Test0
public class Test {
    public static void main(String[] args) {
        Etudiant[] etudiants = {new Etudiant("Ali","Info"), new Etudiant("Fatima","GI")};
        //---------------Affichage avec forech
        for(Etudiant etu:etudiants){
            System.out.println("---------Etudiant----------");
            System.out.println("Nom: "+etu.getNom());
            System.out.println("Filiere: "+ etu.getFiliers());
        }
        //-------------Affichage avec for----------
        for(int k=0;k< etudiants.length;k++){
            System.out.println("---------Etudiant"+(k+1)+"----------");
            System.out.println("Nom: "+etudiants[k].getNom());
            System.out.println("Filiere: "+ etudiants[k].getFiliers());
        }
    }
}
