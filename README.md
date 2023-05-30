# Practica
#include <iostream>
using namespace std;

// Prototipo de la función para obtener el signo zodiacal
string obtenerSignoZodiacal(int dia, int mes);

int main() {
    int dia, mes;

    // Solicitar el día de nacimiento al usuario
    cout << "Ingrese el día de nacimiento: ";
    cin >> dia;

    // Solicitar el mes de nacimiento al usuario
    cout << "Ingrese el mes de nacimiento: ";
    cin >> mes;

    // Obtener el signo zodiacal llamando a la función obtenerSignoZodiacal
    string signoZodiacal = obtenerSignoZodiacal(dia, mes);

    // Mostrar el signo zodiacal resultante
    if (signoZodiacal != "")
        cout << "Tu signo zodiacal es: " << signoZodiacal << endl;
    else
        cout << "Fecha de nacimiento inválida." << endl;

    return 0;
}

// Implementación de la función para obtener el signo zodiacal
string obtenerSignoZodiacal(int dia, int mes) {
    string signo = "";

    // Determinar el signo zodiacal basado en el día y mes de nacimiento
    if ((mes == 1 && dia >= 20) || (mes == 2 && dia <= 18))
        signo = "Acuario";
    else if ((mes == 2 && dia >= 19) || (mes == 3 && dia <= 20))
        signo = "Piscis";
    else if ((mes == 3 && dia >= 21) || (mes == 4 && dia <= 19))
        signo = "Aries";
    else if ((mes == 4 && dia >= 20) || (mes == 5 && dia <= 20))
        signo = "Tauro";
    else if ((mes == 5 && dia >= 21) || (mes == 6 && dia <= 20))
        signo = "Géminis";
    else if ((mes == 6 && dia >= 21) || (mes == 7 && dia <= 22))
        signo = "Cáncer";
    else if ((mes == 7 && dia >= 23) || (mes == 8 && dia <= 22))
        signo = "Leo";
    else if ((mes == 8 && dia >= 23) || (mes == 9 && dia <= 22))
        signo = "Virgo";
    else if ((mes == 9 && dia >= 23) || (mes == 10 && dia <= 22))
        signo = "Libra";
    else if ((mes == 10 && dia >= 23) || (mes == 11 && dia <= 21))
        signo = "Escorpio";
    else if ((mes == 11 && dia >= 22) || (mes == 12 && dia <= 21))
        signo = "Sagitario";
    else if ((mes == 12 && dia >= 22) || (mes == 1 && dia <= 19))
        signo = "Capricornio";

    return signo;
}
