# Instalación de Proxmox Mail Gateway en una Máquina Virtual en Proxmox VE

## Requisitos Previos

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos:

- **CPU**: Procesador moderno compatible con 64 bits.
- **Memoria RAM**: Mínimo 2 GB, se recomienda 4 GB o más.
- **Almacenamiento**: Al menos 32 GB de espacio en disco.
- **Red**: Tarjeta de red compatible.
- **Sistema Operativo del Host**: Proxmox VE instalado y configurado.

## Paso 1: Descargar la ISO de Proxmox Mail Gateway

1. **Descargar la ISO**:
   - Descarga la ISO de Proxmox Mail Gateway desde el siguiente enlace: [ISO de Proxmox Mail Gateway](https://www.proxmox.com/en/downloads/proxmox-mail-gateway/iso/proxmox-mail-gateway-8-1-iso-installer).

## Paso 2: Subir la ISO a Proxmox VE

1. **Acceder a la interfaz web de Proxmox VE**:
   - Abre un navegador web y dirígete a la IP de tu servidor Proxmox VE.
   - Inicia sesión con tus credenciales.

2. **Subir la ISO**:
   - En el panel lateral, selecciona el nodo donde deseas crear la VM.
   - Ve a la pestaña "Content" del almacenamiento donde deseas subir la ISO.
   - Haz clic en "Upload" y selecciona la ISO descargada.

## Paso 3: Crear la Máquina Virtual

1. **Crear una nueva VM**:
   - En el panel lateral, selecciona el nodo donde deseas crear la VM.
   - Haz clic en "Create VM".
   - Configura la VM con los siguientes parámetros:
     - **Nombre**: Proxmox Mail Gateway
     - **OS**: Selecciona "Use CD/DVD disc image file (iso)" y elige la ISO de Proxmox Mail Gateway que subiste.
     - **System**: Usa las configuraciones predeterminadas.
     - **Hard Disk**: Asigna al menos 32 GB.
     - **CPU**: Asigna al menos 2 CPU cores.
     - **Memory**: Asigna al menos 2 GB (recomendado 4 GB o más).
     - **Network**: Configura la red según tus necesidades (puente o NAT).

2. **Finalizar la creación de la VM**:
   - Revisa y confirma la configuración de la VM.
   - Haz clic en "Finish".

## Paso 4: Iniciar la Máquina Virtual e Instalar Proxmox Mail Gateway

1. **Iniciar la VM**:
   - Selecciona la VM creada en el panel lateral.
   - Haz clic en "Start" para iniciar la VM.
   - Haz clic en "Console" para acceder a la pantalla de instalación.

2. **Instalación de Proxmox Mail Gateway**:
   - Acepta los términos de licencia.
   - Selecciona el disco donde instalar Proxmox Mail Gateway.
   - Configura las opciones de idioma y zona horaria.
   - Establece la contraseña de root y proporciona un email para recibir alertas.
   - Configura el FQDN, la IP del servidor, la puerta de enlace y los DNS.
   - Revisa y confirma la configuración.
   - Completa la instalación y reinicia la VM.

## Paso 5: Acceder a la Interfaz Web de Proxmox Mail Gateway

1. **Acceder a la interfaz web**:
   - Abre un navegador web y dirígete a `https://<IP_DEL_MAIL_GATEWAY>:8006`.
   - Ignora cualquier advertencia de certificado de seguridad no confiable.

2. **Iniciar sesión**:
   - Usuario: `root`
   - Contraseña: La contraseña de root configurada durante la instalación.

3. **Configurar y gestionar Proxmox Mail Gateway**:
   - Una vez iniciada la sesión, tendrás acceso a la interfaz de administración de Proxmox Mail Gateway donde podrás configurar y gestionar tus políticas de correo.

## Video Tutorial

Puedes ver un video tutorial detallado del proceso de instalación en el siguiente enlace: [Proxmox Mail Gateway Installation Tutorial](https://www.youtube.com/watch?v=94W16qtx8n8).
