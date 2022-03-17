# PB0022086161HERMILO-

// HERMILO PALOMEQUE GOMEZ // GRUPO 001 16/03/21 
#include <iostream>
#include <string>

using namespace std;

struct cita
{
    char NdP [100], HdT, tratamiento[100], desc[100];
    float T = 0, PreU, PUT;
    int opcion, HdT, CdT;

};

int main() 
{
    int opcion, op, i, j; 
    cita cliente [3]; 

    while (opcion == 1) 
    {
        cout << "-----Elija una opcion segun el numero-----" << endl;
        cout << " 1 Agendar cita " << endl;
        cout << " 2 Modificar cita " << endl;
        cout << " 3 Eliminar cita" << endl;
        cout << " 4 Lista de citas vigentes" << endl;
        cout << " 5 Salir" << endl;
        cin >> opcion;

        switch (opcion)
        {
            
        case 1:

            for (i = 0; i < 3; i++)
            {
                cout << " --- Agendar cita --- " << endl;
                cout << "Numero de registro: " << i + 1 << endl;
                cout << " Ingrese el nombre del paciente" << endl;
                cin >> cliente[i].NdP;
                cin.getline(cliente[i].NdP , 100, '\n');

                cout << " Ingrese el tratamiento" << endl;
                cin >> cliente[i].tratamiento;
                cin.getline(cliente[i].tratamiento, 100, '\n');

                cout << " Ingrese la hora de tratamiento" << endl;
                cin >> cliente[i].HdT;
                cin.getline(cliente[i].HdT, 100, '\n');

                cout << " Ingrese la descripcion del tratamiento" << endl;
                cin >> cliente[i].desc;
                cin.getline(cliente[i].desc, 100, '\n');

                cout << " Ingrese el precio unitario del tratamiento" << endl;
                cin >> cliente[i].PUT;
                cin.getline(cliente[i].PUT, 100, '\n');

                cout << " Ingrece el precio unitario" << endl;
                cin >> cliente[i].PreU;
                cin.getline(cliente[i].PreU, 100, '\n');

                cout << " Ingrese la cantidad del tratamiento" << endl;
                cin >> cliente[i].CdT;
                cin.getline(cliente[i].CdT, 100, '\n');
               
                cout << " ---------------------- " << endl;
                cliente[i].T = cliente[i].PreU * cliente[i].CdT;
                cout << "El total es:" << cliente[i].T << endl;

            }

            break;

        case 3:
            cout << "ingrese el numero registro";
            cin >> j;
            j = j - 1;
            cout << "ingrese que desea modificar: "<< endl;

            cin >> op;


        case 4:
            for (i = 0; i < 3; i++)
            {
                cout<< "------------------------" << endl;
                cout << "Numero de registro: " << i + 1 << endl;
                cout<< cliente[i].NdP <<endl;
                cout<< cliente[i].tratamiento <<endl;
                cout<< cliente[i].HdT <<endl;
                cout<< cliente[i].desc <<endl;
                cout<< cliente[i].PUT <<endl;
                cout<< cliente[i].PreU <<endl;
                cout<< cliente[i].CdT <<endl;
                cout<< cliente[i].T <<endl;
                
                
            }

            break;

        }
        


        cout << "Desea volver al menu?" << endl;
        cout << "1 Para Sí,2 para no" << endl;
        cin >> opcion;

    } 

    return 0;
}
