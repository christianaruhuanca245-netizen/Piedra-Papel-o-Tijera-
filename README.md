#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main(){
    srand(time(NULL));
    int usuario = 0;
    int computadora = 0;
    cout << "Piedra Papelt o Tijera" << endl;
    cout << "1) Piedra" 
    cout << "2) Papel" 
    cout << "3) Tijera" 
    cin >> usuario;

    if(usuario == 1){
        cout << "Tu elegiste Piedra" << endl;
    }
    else if(usuario == 2){
        cout << "Tu elegiste Papel" << endl;
    }
    else{
        cout << "Tu elegiste Tijera" << endl;
    }

    computadora = rand()%3+1;
    if(computadora == 1){
        cout << "La computadora elige Piedra" << endl;
    }
    else if(computadora == 2){
        cout << "La computadora elige Papel"<< endl;
    }
    else{
        cout << "La computadora elige Tijera" << endl;
    }

    // match
    if(usuario == computadora){
        cout << "Empate" << endl;
    }
    // Usuario --> Piedra
    else if(usuario == 1){
        if(computadora == 2){
            cout << "Perdedor!" << endl;
        }
        if(computadora == 3){
            cout << "Ganador!" << endl;
        }
    }
    // Usuario --> Papel
    else if(usuario == 2){
        if(computadora == 1){
            cout << "Ganador!" << endl;
        }
        if(computadora == 3){
            cout << "Perdedor!" << endl;
        }
    }
    // Usuario --> Tijera
    else if(usuario == 3){
        if(computadora == 1){
            cout << "Perdedor!" << endl;
        }
        if(computadora == 2){
            cout << "Ganador!" << endl;
        }
    }
    return 0;




}
