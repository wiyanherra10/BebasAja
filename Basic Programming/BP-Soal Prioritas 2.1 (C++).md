#include <iostream>

void drawXYZ(int height) {
  for (int i = 1; i <= height; i++) {
    if (i % 3 == 0) {
      std::cout << "X" << std::endl;
    } else if (i % 2 == 1) {
      std::cout << "Y" << std::endl;
    } else {
      std::cout << "Z" << std::endl;
    }
  }
}
