# wetterstation
#include <stdio.h>

#define MAX_CITY_NAME_LENGTH 50

struct Wetterdaten {
    char stadt[MAX_CITY_NAME_LENGTH];
    float temperatur;     // Temperatur in Celsius
    float windgeschwindigkeit;  // Windgeschwindigkeit in Metern pro Sekunde
    float niederschlag;   // Niederschlag in Millimetern
    float luftdruck;      // Luftdruck in hPa (Hektopascal)
};

int main() {
    // Definiere ein Array von Strukturen Wetterdaten, um Wetterdaten für 10 Städte zu speichern
    struct Wetterdaten deutscheStaedte[10] = {
        {"Berlin", 20.5, 5.7, 0.0, 1012.3},
        {"Hamburg", 18.2, 4.9, 1.2, 1010.5},
        {"München", 22.8, 6.3, 0.0, 1015.0},
        {"Köln", 19.6, 4.2, 0.8, 1011.8},
        {"Frankfurt", 21.4, 5.1, 0.0, 1013.2},
        {"Stuttgart", 23.0, 5.9, 0.0, 1014.7},
        {"Düsseldorf", 19.8, 4.5, 0.4, 1011.5},
        {"Dortmund", 18.5, 4.0, 0.6, 1012.0},
        {"Essen", 19.2, 4.3, 0.3, 1011.2},
        {"Bremen", 17.9, 4.7, 1.5, 1009.8}
    };

    // Drucke Wetterdaten für jede Stadt aus
    printf("Wetterdaten für Städte in Deutschland:\n");
    printf("--------------------------------------\n");
    for (int i = 0; i < 10; ++i) {
        printf("Stadt: %s\n", deutscheStaedte[i].stadt);
        printf("Temperatur: %.1f°C\n", deutscheStaedte[i].temperatur);
        printf("Windgeschwindigkeit: %.1f m/s\n", deutscheStaedte[i].windgeschwindigkeit);
        printf("Niederschlag: %.1f mm\n", deutscheStaedte[i].niederschlag);
        printf("Luftdruck: %.1f hPa\n", deutscheStaedte[i].luftdruck);
        printf("\n");
    }

    return 0;
}
