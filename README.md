# terminalFontStyles
a cross platform c++ library to write colored text on terminal
### usage:
```c++
std::cout << TEXT_BG_BLACK_BRIGHT_YELLOW << "WARNING!" << TEXT_RESET << std::endl;
std::cout << TEXT_BLUE << "Deep Water" << TEXT_RESET << std::endl;
```
- the following macros "TEXT_BOLD" and "TEXT_UNDERLINE are plarform and terminal dependent styles
```c++
std::cout << TEXT_BOLD << TEXT_UNDERLINE << TEXT_BG_YELLOW_GREEN << "GARDEN" << TEXT_RESET << std::endl;
```
- the fuctions "TEXT_RGB" and "TEXT_BG" require use of a *nix enviroment and a terminal that support a hight color depth like alacritty
```c++
//generating a color rage on terminal!
for ( int i = 0; i < 256; i++ )
  std::cout << BG_RGB(i, 0 , 0) << " ";
std::cout << std::endl;

for ( int i = 0; i < 256; i++ )
  std::cout << BG_RGB(0, i, 0) << " ";
std::cout << std::endl;

for ( int i = 0; i < 256; i++ )
  std::cout << BG_RGB(0, 0, i) << " ";
std::cout << TEXT_RESET << std::endl;

for ( int i = 0; i < 256; i++)
  std::cout << TEXT_RGB(i, i, i) << "A";
std::cout << TEXT_RESET << std::endl;
```
### result:
![](https://i.ibb.co/d6Q3k4f/terminal-Font-Styles-Demo-Capture.png)
