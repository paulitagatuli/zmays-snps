Capitulo 2

Command + barra. Abrir terminal. Es case sensitive
pwd te dice tu working directory
mkdir zmays-snps Crea la carpeta zmays-snps en tu working directory
cd zmays-snps cambia el working directory a ese
mkdir data Crea la carpeta data
mkdir data/seqs scripts analysis Crea la carpeta seis dentro de data, crea scripts y analysis dentro de smays-snps
ls -l Te muestra todo lo que hay en el working directory, separando x lineas

rm -r remueve recurisvamente lo que le indiques
rm -rf remueve recusrivamente y todo, sin warnings
../path  El .. significa "el directorio anterior"

touch/README crea un .txt vacío en tu working directory
open README abre el txt
echo Te imprime cosas en la terminal
mkdir -p zmays-snps/{data/seqs,scripts,analysis} Llegas al mismo resultado con una sola linea de código, -p te permite crear directorios cuyo parental aun no existe, ej: data para crear seqs
touch seqs/zmays{A,B,C}_R{1,2}.fastq crea 6 files .fastq en seqs que se llaman "zmaysA_R1" o "zmaysA_R1", lo mismo para B y C.
ls zmaysB* Te muestra todos los files que se llaman "zmaysB", en este caso el R1 y R2.
ls zmaysB*fastq Ara te devuelve los que se llaman zmaysB y son archivos fastq
ls zmaysB_R?.fastq Te devuelve todos los RN (ojo que ? matches a single characters)  
ls zmays[AB]_R[12].fastq Te devuelve todos los zmays A y B, R1 y R2. Tmb se puede escribir [A-B]
find ./ -name "*.fastq"  Te busca todos los archivos .fastq en tu working directory (por el ./, sino hay que ponerle el path)

Al usar files, poner 0s adelante, es decir 0001,0002,0003 etc, sino se ordenan bizarro
Usar path relativos y no absolutos
No usar espacios para los nombres de archivos y directorios
Es mejor tener muchos subdirectorios con sus archivos intermedios y README

###Documentacion:
Todas lineas de comando que uses en la terminal, valores de parámetros de los software que uses
De donde viene la data, que fecha tiene, de donde la descargaste 
Fecha y version de las database
Como descargaste la data (MySQL, UCSC Genome Browser, etc)
Versiones de software que usaste
Pipeline de lo que hiciste y el orden (diagnostico, alineamiento, curación, etc)