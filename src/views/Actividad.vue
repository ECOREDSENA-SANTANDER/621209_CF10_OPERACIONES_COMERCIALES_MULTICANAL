<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
      // Para cuestionario usar: ActividadController(:cuestionario="cuestionario") 
      // Para parrafo usar: ActividadController(:parrafo="parrafo")
      ActividadController(:cuestionario="cuestionario")
  </template>

<script>
import ActividadController from '@ecored-sena/base-kit/plugin/components/actividad/ActividadController.vue'

export default {
  name: 'ActividadDidactica',
  components: {
    ActividadController,
  },
  data: () => ({
    cuestionario: {
      tema: 'Protocolos de cierre de caja',
      titulo: 'Cuestionario',
      introduccion:
        '<b> Objetivo:</b> Verificar la comprensión de los conceptos fundamentales relacionados con el cierre de la operación, el procedimiento técnico, la clasificación del efectivo y los medios de pago, la validación de documentos de valor, los elementos de seguridad del dinero, el arqueo de caja y la entrega del puesto de trabajo en el <i>retail</i>.',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto: 'El cierre de caja tiene como propósito principal:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Comparar el dinero y documentos de valor existentes en caja con los datos reportados por las ventas y el sistema.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Reorganizar la exhibición de productos al final del día.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Cambiar los precios de los productos vendidos durante la jornada.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Asignar nuevas funciones comerciales al cliente.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 2,
          texto: 'Los protocolos de cierre se aplican principalmente cuando:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Se recibe mercancía nueva en bodega.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Finaliza la operación del <i>retail</i> o se presentan cambios de jornada o turno en caja.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Se diseña una campaña de promoción interna.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Se selecciona el material de empaque para productos frágiles.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 3,
          texto:
            'El procedimiento técnico en el punto de pago se entiende como:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Una estrategia de publicidad para aumentar las ventas.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Una lista de precios sin relación con el recaudo.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Una secuencia de acciones sistematizadas para registrar dinero y formas de pago de manera segura y conforme a los procedimientos.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Un proceso exclusivo para empacar mercancía.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 4,
          texto:
            'Durante el turno, el cajero debe aplicar el procedimiento técnico con concentración para:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Evitar registrar medios de pago electrónicos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Aumentar el tiempo de atención al cliente.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Sustituir el arqueo de caja al cierre.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Prevenir equivocaciones a favor de la empresa o del cliente.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 5,
          texto: 'La orden de compra se caracteriza porque:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Es un documento emitido por la compañía que el cliente usa para adquirir mercancía del almacén.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Es un billete emitido por una entidad bancaria.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Es un comprobante que siempre se cambia totalmente por efectivo.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Es un documento usado solo para arqueos internos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 6,
          texto:
            'Una característica de seguridad de la orden de compra puede ser:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'La ausencia total de numeración.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Marca de agua, papel similar al de un billete y numeración impresa con tinta especial.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Elaboración verbal sin soporte físico.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Uso obligatorio fuera del establecimiento que la emite.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 7,
          texto: 'Los bonos regalo se deben recibir teniendo en cuenta que:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Siempre acumulan puntos por la compra realizada.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Pueden negociarse libremente por dinero en efectivo.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Generalmente deben redimirse en el almacén que los emite y utilizarse por su valor total.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'No requieren verificación de condiciones para ser aceptados.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 8,
          texto: 'La nota cambio se entrega al cliente cuando:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Desea abrir una caja nueva para iniciar su turno.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Solicita autorización bancaria para un cheque.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Compra productos sin pasar por el punto de pago.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Cambia un producto defectuoso o por una situación adversa y la usa como pago en una nueva compra.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 9,
          texto: 'Los bonos recibidos en el punto de pago deben:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Estar en perfecto estado, sin enmendaduras, tachones o borrones, y dentro de la fecha de vencimiento.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Recibirse aunque estén vencidos si el cliente insiste.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Cambiarse siempre por dinero en efectivo.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Aceptarse aunque no estén autorizados para el almacén.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 10,
          texto:
            'En los <i>tickets</i>, una condición de seguridad que debe revisar el cajero es:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Que no tengan ningún desprendible.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Que el valor coincida en el bono y en el desprendible, además de revisar marcas de agua y vigencia.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Que estén rayados para demostrar uso previo.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Que no tengan logos ni información visible.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 11,
          texto: 'En una transacción con tarjeta débito, normalmente:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Se exige la cédula porque el sistema no pide clave.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'El valor debe ser siempre superior al valor de la compra.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'El sistema solicita la clave y el valor se descuenta directamente de la cuenta bancaria del cliente.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'El cajero debe anotar manualmente el código de seguridad de la tarjeta.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 12,
          texto:
            'En una transacción con tarjeta de crédito, el cajero debe tener presente que:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'No se debe verificar la identidad del titular.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'La tarjeta puede ser usada por cualquier persona sin autorización.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'El sistema siempre exige clave y nunca requiere cédula.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Es personal e intransferible y se debe requerir la cédula del titular de la tarjeta.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 13,
          texto: 'Una característica de seguridad de las tarjetas es:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La apariencia general del plástico, el chip, el icono de pago sin contacto, la fecha de vencimiento y el panel de firma.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'La ausencia de datos de contacto de la entidad emisora.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Que el panel de firma se desprenda con facilidad.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Que los logotipos estén borrosos para evitar copia.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 14,
          texto: 'Para recibir un cheque personal, es necesario verificar que:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Esté elaborado con lápiz y permita tachones.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Esté girado a nombre del almacén, tenga cantidad igual en números y letras, fecha completa y firma autógrafa.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'No tenga firma del girador.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'La ciudad y la fecha estén incompletas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 15,
          texto:
            'La autorización de cheques personales debe gestionarse según:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'La opinión del cliente al momento de pagar.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'La cantidad de bolsas utilizadas para empacar.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'El procedimiento y límite definido por la compañía, solicitando autorización cuando corresponda.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'El tipo de productos que se exhiben en góndola.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 16,
          texto:
            'Cuando se sospecha de la autenticidad de un billete, una práctica adecuada es:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Aceptarlo sin revisión para evitar demoras.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Romperlo para comprobar su resistencia.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Guardarlo sin reportarlo al cierre.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Compararlo con otro billete auténtico y revisar sus elementos de seguridad.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 17,
          texto:
            'Entre los elementos generales de seguridad de los billetes actuales se encuentran:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Relieves, marcas de agua, hilos de seguridad, reacción a luz ultravioleta, microtextos y variación de color.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Únicamente el tamaño del papel.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Solo la firma escrita por el cajero.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'La ausencia de imágenes coincidentes.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 18,
          texto: 'El arqueo de caja consiste en:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Reemplazar el informe diario por una conversación informal.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Verificar si el efectivo y documentos físicos de pago coinciden con el dinero reportado por ventas en cada caja.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto:
                'Eliminar los comprobantes de pago para evitar acumulación.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Modificar los valores registrados en el sistema sin soporte.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 19,
          texto: 'Una situación que puede complicar el arqueo de caja es:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Tener todos los soportes organizados y facturación controlada.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Registrar cada operación en un sistema automatizado.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Recibir distintos documentos de pago combinados, no tener control de facturación o mover dinero para gastos.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Cerrar el puesto de pago sin operaciones durante el día.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 20,
          texto: 'La entrega a conformidad del puesto de trabajo implica que:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Puede quedar dinero en efectivo o bonos en la caja para el siguiente turno.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'No es necesario reportar soportes al departamento de recaudo.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'El cajero solo entrega lo que recuerde de la jornada.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Lo registrado durante la jornada debe coincidir con lo presentado al finalizar, siguiendo políticas y protocolos.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: 'Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado:
        'Ha superado la actividad y demuestra comprensión de los protocolos de cierre de caja, el manejo de medios de pago y el arqueo de caja.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
