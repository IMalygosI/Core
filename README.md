# Core Часть 1 без клавиатуры, если нужно с клавиатурой смотри в ветках.
![image](https://github.com/IMalygosI/Core/assets/67872855/90d5f65b-626d-431f-acc9-0ea3d5ef70c6)


Для начала откройте cmd и загрузите: (gcc, nasm, qemu)\n
Чтобы запустить соберите проект введя такие команды: "ВАЖНО! Перед этим скачайте файл из репозитория и разархивируйте его"
1.Выполнить команду: nasm -f elf32 kernel.asm -o kasm.o
2.Выполнить команду: gcc -m32 -c kernel.c -o kc.o
3.Выполнить команду: gcc -fno-stack-protector -m32 -c kernel.c -o kc.o
4.Выполнить команду: ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o
5.Запустить на эмуляторе: qemu-system-i386 -kernel kernel
