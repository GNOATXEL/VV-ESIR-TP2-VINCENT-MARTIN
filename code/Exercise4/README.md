# exo 4

On observe que dans un fichier Maison.java. Dans ce dernier, l'attribut adresse n'a pas de getter. Cet attribut va nous permetre de tester  si notre fonction est bonne. C'est a dire si elle nous renvoie bien l'ensemble des attributs sans getter.
On observe que dans notre fichier Public ElementsPrinter.java on à ajouté:

```java
 public void attributs_that_dont_get_getter(){
        List<String> no_getter = new ArrayList<String>();
        for (int i =0; i<private_attributs.size();i++){
            String[] temp_attribut = private_attributs.get(i).split(" ");
                    boolean got_getter=false;
            for (int y=0;y<public_method.size();y++){
                String[] temp_methode=public_method.get(y).split(" ");
                if (temp_methode[2].startsWith("get")){
                    if ((temp_methode[2].substring(3,temp_methode[2].length()-2)).toLowerCase().equals(temp_attribut[2].toLowerCase().substring(0,temp_attribut[2].length()-1))){
                       got_getter=true;
                    }
                } else if (temp_methode[2].startsWith("is")) {
                    if ((temp_methode[2].substring(2,temp_methode[2].length()-2)).toLowerCase().equals(temp_attribut[2].toLowerCase().substring(0,temp_attribut[2].length()-1))){
                        got_getter=true;
                    }
                }
            }
            if(!got_getter){
            no_getter.add(private_attributs.get(i));}
        }
        System.out.println(no_getter);
        }
```
```java
        public void visit(FieldDeclaration declaration,Void arg){
            if(!declaration.isPrivate()) return;
            System.out.println("  " + declaration.toString());
            private_attributs.add(declaration.toString());
```
        }
    }
