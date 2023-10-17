# Airflow

**By: Dexne**

Apache Airflow es una plataforma de código abierto diseñada para orquestar y automatizar flujos de trabajo complejos. Su arquitectura se basa en programación dirigida por tareas, permitiendo a los usuarios definir, programar y supervisar secuencias de tareas interconectadas de manera eficiente. Airflow facilita la creación de flujos de trabajo escalables y flexibles al utilizar DAGs (Grafos Acíclicos Dirigidos) para representar las relaciones entre las tareas. Ofrece una interfaz web intuitiva para monitorear y administrar tareas, además de un motor de ejecución confiable. Con soporte para numerosos conectores y una comunidad activa, Airflow es una herramienta esencial para la automatización de procesos y la administración de datos a gran escala.

Si quieres saber un poco más al respecto acerca de esta poderosa herramienta puedes darte una vuelta por la documentación oficial.

[Airflow - Documentación oficial](https://airflow.apache.org/docs/apache-airflow/stable/public-airflow-interface.html)

**¿Cómo funciona?**

Apache Airflow funciona a través de una arquitectura flexible y escalable que permite la automatización y orquestación de flujos de trabajo.

1. Definición de tareas: Los usuarios definen sus flujos de trabajo como DAGs (Grafos Acíclicos Dirigidos), que son representaciones visuales de las tareas y sus dependencias. Cada tarea puede ser un script, un comando, una operación de transferencia de datos u otra acción.

2. Planificación y programación: Airflow utiliza un programador para planificar cuándo se ejecutarán las tareas en función de sus dependencias y horarios especificados. Puedes establecer horarios cron, disparadores manuales o condiciones específicas para iniciar tareas.

3. Ejecución y monitoreo: Cuando llega el momento de ejecutar una tarea, Airflow la asigna a un trabajador. Los trabajadores son máquinas que ejecutan las tareas y registran su estado y resultados. Puedes monitorear el progreso y el estado de las tareas a través de la interfaz web de Airflow.

4. Gestión de errores y reintentos: Airflow maneja automáticamente los errores y reintentos de tareas, lo que garantiza la confiabilidad de los flujos de trabajo. Puedes configurar políticas de reintentos y notificaciones de fallos.

5. Conexiones y conectores: Airflow admite una amplia variedad de conectores que facilitan la integración con sistemas externos, bases de datos, servicios en la nube y más. Esto permite la transferencia de datos y la interacción con otros sistemas.

6. Escalabilidad y paralelismo: Airflow es altamente escalable y puede ejecutar tareas en paralelo en múltiples trabajadores, lo que lo hace adecuado para flujos de trabajo complejos y a gran escala.

**Instalación**

Cabe mencionar que la instalación puede resultar un poco complicada para usuarios de windows, en mi caso yo me encuentro usando Fedora Linux, una distribución basada en Red Hat.

Instalación por medio de PIP:

pip install apache-airflow

**Inicializar la db**

Inicializa la base de datos de Airflow. Airflow utiliza una base de datos para gestionar sus metadatos y programación. Puedes elegir entre SQLite, PostgreSQL, MySQL, o MSSQL como backend de la base de datos. A continuación, se muestra un ejemplo de cómo inicializar la base de datos con SQLite:

airflow db init

Si prefieres utilizar otro motor de base de datos, asegúrate de tenerlo instalado y configura la conexión en el archivo de configuración de Airflow (airflow.cfg).

**inicializar el webserver de Airflow**

airflow webserver --port 8080

Esto iniciará el servidor web de Airflow en el puerto 8080. Puedes acceder a la interfaz web de Airflow en tu navegador ingresando la dirección http://localhost:8080.

también debemos de inicializar el scheduler:

airflow scheduler

El scheduler es responsable de programar y ejecutar las tareas programadas.

Con esto deberemos de tener bien instalado Airflow y listo para trabajar.

A continuación te proporciono fotos como evidencia de la instalación y ejecución del proyecto:

[Entorno virtual para trabajar](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/Entornos_virtuales.jpeg)

[Instalación de Airflow](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/instalacion_de_airflow.jpeg)

[Inicializar la db](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/inicializar_db.jpeg)

[Inicializar scheduler](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/activar_scheduler.jpeg)

[Levantar el webserver](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/Levantar_servidor.jpeg)

[loggin](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/loggin_localhost.jpeg)

[verificación de la creación del DAG](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/dashboard.jpeg)

[Ejecución](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/Ejecucion.jpeg)

[Ejecución](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/Ejecucion_1.jpeg)

[ejecucion manual](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/ejecucion_manual.jpeg)

[Calendar](https://github.com/Dexne/Airflow_Fault_Tolerant/blob/main/assets/Calendar.jpeg)
