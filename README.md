<h1 align="center">Core Часть 1 без клавиатуры, если нужно с клавиатурой смотри в ветках.</h1><br>

![image](https://github.com/IMalygosI/Core/assets/67872855/90d5f65b-626d-431f-acc9-0ea3d5ef70c6)


Для начала установите ОС "К примеру KDE NEON", затем откройте cmd и загрузите: (gcc, nasm, qemu)<br>

Чтобы запустить проект вам необходимо ввести такие команды: "ВАЖНО! Перед этим скачайте файл из репозитория и разархивируйте его"<br>
1.Выполнить команду: nasm -f elf32 kernel.asm -o kasm.o<br>
2.Выполнить команду: gcc -m32 -c kernel.c -o kc.o<br>
3.Выполнить команду: gcc -fno-stack-protector -m32 -c kernel.c -o kc.o<br>
4.Выполнить команду: ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o<br>
5.Запустить на эмуляторе: qemu-system-i386 -kernel kernel<br>


<h1 align="center">Выполнил: студент группы:ИП2К-22 Удальцов Дмитрий Игоревич</h1><br>
