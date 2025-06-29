# Juego-Adivina-Quien
Este es un proyecto de juego basico de escritorio estilo “Adivina Quién” desarrollado en **Visual Basic** usando **Visual Studio**. El objetivo del juego es descubrir qué personaje ha sido seleccionado al azar por el usuario, haciendo que la computadora haga preguntas basadas las características de tu personaje seleccionado.

---

## 🧩 Características

- Interfaz gráfica sencilla e intuitiva.
- Personajes con distintas características físicas (gafas, color de cabello, pecas, etc.).
- Sistema de preguntas con botones de sí/no.


---

## 🛠 Requisitos

- Visual Studio 2019 o superior
- .NET Framework 4.7.2 o compatible
- Windows 10/11

---
## 📁 Estructura del proyecto

```
Juego-Adivina-Quien
├── Juego_Adivina_Quien.vb
└── README.md
```

## ▶️ Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
  
   ```
2. Abre el archivo `.sln` en Visual Studio.
3. Presiona **F5** o haz clic en **Iniciar** para compilar y ejecutar.

## 🧠 Lógica del juego 

    Public Class Form1
    Dim paso As Integer = 0

    Private Sub AutoraToolStripMenuItem_Click(sender As Object, e As EventArgs) Handles AutoraToolStripMenuItem.Click
        MsgBox("Hairaly Diaz")
    End Sub

    Private Sub SalirToolStripMenuItem_Click(sender As Object, e As EventArgs) Handles SalirToolStripMenuItem.Click
        End
    End Sub

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        
        IniciarJuego()
    End Sub

    Private Sub IniciarJuego()
        paso = 1
        Label1.Text = "¿Es mujer?"
        Button1.Enabled = True
        Button2.Enabled = True
    End Sub

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
       
        Avanzar(True)
    End Sub

    Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click

        Avanzar(False)

    End Sub

    Private Sub Avanzar(respuesta As Boolean)

        If paso = 1 Then
            If respuesta Then
                paso = 2
                Label1.Text = "¿Tiene el cabello rubio?"
            Else
                paso = 10
                Label1.Text = "¿Tiene barba?"
            End If
            
        ElseIf paso = 2 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Carla"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
                Fin()
            Else
                paso = 3
                Label1.Text = "¿Tiene el cabello pelirrojo?"
            End If

        ElseIf paso = 3 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Elena"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
                Fin()
            Else
                paso = 4
                Label1.Text = "¿Tiene gafas?"
            End If

        ElseIf paso = 4 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Ana"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
                Fin()
            Else
                paso = 5
                Label1.Text = "¿Tiene el cabello negro?"
            End If

        ElseIf paso = 5 Then
            If respuesta Then
                paso = 6
                Label1.Text = "¿Tiene pecas?"
            Else
                Label1.Text = "Personaje no encontrado."
                Fin()
            End If

        ElseIf paso = 6 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Gabriela"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
            Else
                Label1.Text = "Personaje no encontrado."
            End If
            Fin()

        ElseIf paso = 10 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Bruno"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
                Fin()
            Else
                paso = 11
                Label1.Text = "¿Usa sombrero?"
            End If

        ElseIf paso = 11 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Diego"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
                Fin()
            Else
                paso = 12
                Label1.Text = "¿Usa lentes de sol?"
            End If

        ElseIf paso = 12 Then
            If respuesta Then
                Label1.Text = "Tu personaje es: Fabio"
                MessageBox.Show("¡Yay! 🎉 Adiviné tu personaje ", "¡Correcto!", MessageBoxButtons.OK, MessageBoxIcon.Information)
            Else
                Label1.Text = "Personaje no encontrado."
            End If
            Fin()
        End If
    End Sub

    Private Sub Fin()
        Button1.Enabled = False
        Button2.Enabled = False

    End Sub

    Private Sub Button3_Click(sender As Object, e As EventArgs) Handles Button3.Click
        IniciarJuego()
    End Sub
    End Class
```

## 📸 Capturas de pantalla
![Captura de pantalla 2025-06-28 225809](https://github.com/user-attachments/assets/e5ade118-7e0b-408c-ba81-0c352ced63f5)
![Captura de pantalla 2025-06-28 225849](https://github.com/user-attachments/assets/2dcf2320-e598-44c6-be2b-daaca04b2e4d)

