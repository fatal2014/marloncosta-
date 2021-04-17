# marloncosta-
EA1 programação aplicada
#include <iostream>


using namespace std;

void comparar(string word){
        
        char alfabeto[8][4]= { {'a','b','c',' '},{'d','e','f',' '},{'g','h','i',' '},
                            {'j','k','l',' '},{'m','n','o',' '},{'p','q','r','s'},
                            {'t','u','v',' '},{'w','x','y','z'}};
        
         for(int y =0; y < sizeof(alfabeto); y++){
            for (int z = 0; z < word.length(); z++){    
                for(int x =0; x < 4; x++){
                    if(word[z] == alfabeto[y][x]){
                        cout<<'#'<<(y+2)<<'='<<(x+1)<<endl;
                        break;
                    }  
                }
                            
            }
        }
}

int main(){

    string saida = "r";
    string palavra;
    do{
        cout<<"escreva uma palavra:"<<endl;
        
        cin>>palavra;
        if(palavra.length() < 50){
            comparar(palavra);
            
        }else{
            cout<<"escreva palavras de 50 caracteres no máximo!"<<endl;
        }
        
        cout<<"quer digitar mais alguma palavra? s/n"<<endl;
        cin>>saida;
    }while(saida =="r") ;
}
