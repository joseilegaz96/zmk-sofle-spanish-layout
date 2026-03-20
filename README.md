# Sofle con layout en Español 

Fork modificado del a741725193/zmk-sofle para adaptarlo al layout español junto con la herramienta de zmk-locale-generator los keymap de español estan generados en config/keys_es.h.


## Instrucciones de uso

Si quieres añadir o modificar algunas keymap basta con irse al config/keys_es.h con sus codigos de referencia copiar lo que te interese irse al config/eyelash_sofle.keymap y poner &kp delante con el codigo de la tecla.

Ejemplo
Supongamos que quiero añadir la ñ:
   - #define ES_N_TILDE (ZMK_HID_USAGE(HID_USAGE_KEY, HID_USAGE_KEY_KEYBOARD_SEMICOLON_AND_COLON)) esto es como esta definido la ñ en el keys_es.h.
   - Ahora nos vamos al eyelash_sofle.keymap

   - Esto es la capa layer0 añadimos la ñ al lado de la l para eso ponemos el codigo de la ñ(ES_N_TILDE) para eso vamos a la tecla que esta al lado de la l y lo añadimos &kp ES_N_TILDE como se puede ver abajo.


    /
     keymap { 
        compatible = "zmk,keymap";
        layer0 {
         bindings = <
           &kp ESC      &kp N1     &kp N2     &kp N3     &kp N4     &kp N5     &kp UP_ARROW &kp N6     &kp N7     &kp N8     &kp N9     &kp N0     &kp BACKSPACE
           &kp TAB      &kp Q      &kp W      &kp E      &kp R      &kp T      &kp DOWN_ARROW &kp Y     &kp U      &kp I      &kp O      &kp P      &kp ES_C_CEDILLA
           &kp CAPS     &kp A      &kp S      &kp D      &kp F      &kp G      &kp LEFT_ARROW &kp H     &kp J      &kp K      &kp L      &kp ES_N_TILDE &kp ES_ACUTE
           &kp LSHFT    &kp Z      &kp X      &kp C      &kp V      &kp B      &kp RIGHT_ARROW &kp N    &kp M      &kp COMMA  &kp DOT    &kp ES_LT  &kp ENTER
           &kp C_MUTE   &kp LCTRL  &kp LEFT_GUI &kp LEFT_ALT &kp SPACE &mo 1   &kp ENTER &mo 2 &kp SPACE &kp RALT  &kp LCTRL  &kp DELETE
         >;

         sensor-bindings = <&inc_dec_kp C_VOLUME_UP C_VOL_DN>;
         display-name = "Escritura";
    };

 ## Distrubución de las teclas
<img width="984" height="1609" alt="my_keymap" src="https://github.com/user-attachments/assets/c15d1e44-b1a2-486b-9208-251028a1f273" />
