# Proyecto--Taller-Integrador---Grupo-4
##Link Reunion:
https://meet.google.com/xjn-oede-rrs

## Link Diagrama de Gantt:
https://docs.google.com/spreadsheets/d/1RLvCeBbs8q7GYEhUyf99uF2kCLAGFvYE/edit?usp=sharing&ouid=103265704217449199971&rtpof=true&sd=true

## Documento Escrito
https://prism.openai.com/?u=4f71073c-6474-493f-a1eb-b1f56d1139e6&pg=1&m=main.tex&d=7 

## Retrospectiva_Sprints 
https://docs.google.com/spreadsheets/d/1yZAs3TcN8QVUfOVWJbkrDeOPjbkcMm1C/edit?gid=1476389224#gid=1476389224


## JERARQUÍA Y ESTRUCTURA DEL PROYECTO

```text
/ (Raíz del Repositorio)
├── docs/                      # Documentación y hojas de datos
│   ├── datasheets/            # Datasheets de componentes (MAX8510, APX812, etc.)
│   └── specs/                 # Requerimientos y especificaciones
├── hardware/                  # Proyecto y esquemáticos en Altium Designer
│   ├── libraries/             # Librerías locales de componentes
│   │   ├── SiWA_Project.SchLib
│   │   └── SiWA_Project.PcbLib
│   ├── outputs/               # Archivos de salida y fabricación
│   │   ├── bom/               # Listas de materiales en Excel
│   │   ├── gerbers/           # Archivos Gerber y Drill
│   │   └── pdfs/              # Esquemáticos exportados en PDF
│   ├── SiWA_Main_Board.PrjPcb # Archivo de proyecto principal de Altium
│   ├── Top_Level.SchDoc       # Hoja principal de integración global
│   ├── Sub_Power.SchDoc       # Subsistema 1: Regulación y alimentación
│   ├── Sub_Clock_SPI_UART.SchDoc # Subsistema 2: Reloj 20MHz, Flash SPI y UART
│   ├── Sub_OLED_GPIO.SchDoc   # Subsistema 3: Pantalla OLED, LEDs y GPIOs
│   └── Sub_Reset_SiWA.SchDoc  # Subsistema 4: Circuito de reset e interfaz SiWA
└── firmware/                  # Firmware de prueba y utilidades
     └── test_code/             # Scripts de validación y binarios para Flash
==============================================================================

.PHONY: tree

## Target para imprimir la estructura directa en la terminal al ejecutar 'make tree'
tree:
	@echo "=================================================================="
	@echo "                JERARQUÍA DEL PROYECTO SIWA                       "
	@echo "=================================================================="
	@echo " / (Raíz)"
	@echo " ├── docs/                    -> Datasheets y especificaciones"
	@echo " ├── hardware/                -> Diseño en Altium Designer"
	@echo " │   ├── libraries/           -> Librerías (.SchLib, .PcbLib)"
	@echo " │   ├── outputs/             -> Gerbers, BOM y PDFs"
	@echo " │   ├── Top_Level.SchDoc     -> Esquemático de Integración"
	@echo " │   ├── Sub_Power.SchDoc     -> Esquemático Alimentación"
	@echo " │   ├── Sub_Clock_SPI_UART   -> Esquemático Clock/SPI/UART"
	@echo " │   ├── Sub_OLED_GPIO.SchDoc -> Esquemático OLED/LEDs"
	@echo " │   └── Sub_Reset_SiWA.SchDoc-> Esquemático Reset e Interfaz"
	@echo " └── firmware/                -> Código y binarios de prueba"
	@echo "=================================================================="
