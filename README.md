#!/bin/bash

menu() {

printf "\e[1;92m[\e[0m\e[1;77m1\e[0m\e[1;92m]\e[0m\e[1;93m Visitar enlace \e[0m\n"
printf "\e[1;92m[\e[0m\e[1;77m2\e[0m\e[1;92m]\e[0m\e[1;93m Visitar mi canal \e[0m\n"
read -p $'\n\e[1;92m[\e[0m\e[1;77m*\e[0m\e[1;92m] Choose an option: \e[0m' option

if [[ $option == 1 || $option == 01 ]]; then
am start -a android.intent.action.VIEW -d https:http://barsoocm.com/1Qd1 > /dev/null 2>&1 
elif [[ $option == 2 || $option == 02 ]]; then
am start -a android.intent.action.VIEW -d https://github.com/Teorooa > /dev/null 2>&1 
elif [[ $option == 0 ]]; then
exit 1
else
printf "\e[1;93m [!] Invalid option!\e[0m\n"
sleep 1
menu
fi
}
