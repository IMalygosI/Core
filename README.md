<h1 align="center">Ядро но уже с поддержкой клавиатуры</h1><br>

![Ядро с поддержкой клавиатуры](https://github.com/IMalygosI/Core/assets/67872855/445af22c-3124-4565-981c-a2fc92a6b45a)


Для начала установите ОС "К примеру KDE NEON", затем откройте cmd и загрузите: (gcc, nasm, qemu)<br>

Чтобы запустить проект вам необходимо ввести такие команды: "ВАЖНО! Перед этим скачайте файл из репозитория и разархивируйте его"<br>
1.Выполнить команду: nasm -f elf32 kernel.asm -o kasm.o<br>
2.Выполнить команду: gcc -m32 -c kernel.c -o kc.o<br>
3.Выполнить команду: gcc -fno-stack-protector -m32 -c kernel.c -o kc.o<br>
4.Выполнить команду: ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o<br>
5.Запустить на эмуляторе: qemu-system-i386 -kernel kernel<br>
