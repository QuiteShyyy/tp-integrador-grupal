# tp-integrador-grupal
Trabajo Práctico Integrador Grupal - Universidad de Palermo
# Trabajo Práctico Integrador Grupal

## Universidad de Palermo
**Institución:** Universidad de Palermo  
**Asignatura:** Computacion Aplicada
**Año:** 2026

---

## Participantes del Grupo

| Nombre | Apellido | Legajo |
|--------|----------|--------|
| Dante | Prantt Oviedo | 0158208 |
| Sofia | Mosquera | 0161369 |
| Fernando Jesus | Hidalgo Quispe | 0161781 |
---

## Descripción del Proyecto

Este proyecto implementa la configuración completa de un servidor Linux (Debian 12) con los siguientes componentes:

- **Sistema Operativo:** Debian 12
- **Servidor Web:** Apache2 con soporte PHP 7.3+
- **Base de Datos:** MariaDB
- **SSH:** Autenticación mediante claves RSA
- **Almacenamiento:** Particiones adicionales para datos web y backups
- **Automatización:** Scripts de backup con cron

---

## Estructura del Repositorio

```
tp-integrador-grupal/
├── README.md
├── root/                  # Contenido del home de root
├── etc/                   # Configuraciones del sistema
├── opt/                   # Scripts y programas personalizados
├── www_dir/               # Archivos web
├── backup_dir/            # Backups (opcional)
└── var/                   # Directorios de logs y datos (spliteos)
```

---

## Instalación y Configuración

Ver la documentación completa en `GUIA_PASO_A_PASO.md`

### Requisitos Previos
- Máquina virtual con Debian 12
- 20 GB de almacenamiento (10 GB adicional para particiones)
- 2 GB de RAM (mínimo)

---

## Servicios Configurados

### SSH
- Puerto: 22
- Autenticación: Clave Privada/Pública
- Usuario: root

### Apache/PHP
- Puerto: 80
- DocumentRoot: /www_dir
- Versión PHP: 7.3+

### MariaDB
- Puerto: 3306
- Usuario: lcars
- Base de datos: ingenieria

---

## Backups Automáticos

Los siguientes backups se ejecutan automáticamente:

- **Diariamente a las 00:00:** `/var/log`
- **Lunes, Miércoles, Viernes a las 23:00:** `/www_dir`

Ver script en: `/opt/scripts/backup_full.sh`

---

## Notas Importantes

- La contraseña de root es: `palermo`
- El hostname está configurado como: `TPServer`
- Los archivos de configuración están en `/etc`
- Los scripts personalizados están en `/opt/scripts`

---

## Contacto

Para preguntas, contactar a los integrantes del grupo listados arriba.
