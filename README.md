# Step-24-The-friend-keyword-friend-functions-and-classes-.
#include <iostream>
#include <windows.h>
#include <string>
#include <memory>

class Gamer {
private:
	int health{ 50 };

public:

	friend void restore_health(Gamer& g);
};

void restore_health(Gamer& g) {
	g.health = 100;
	std::cout << "Здоровье взломно: " << g.health << std::endl;
}

 int main(){
	 SetConsoleCP(1251);
	 SetConsoleOutputCP(1251);
	 
	
	 Gamer player;

	 restore_health(player);

	
	 return 0;
 }
