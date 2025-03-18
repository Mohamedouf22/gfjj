from kivy.app import App # type: ignore
from kivy.uix.boxlayout import BoxLayout # type: ignore
from kivy.uix.button import Button # type: ignore
from kivy.uix.label import Label # type: ignore
from kivy.uix.textinput import TextInput # type: ignore

class DeterminantApp(App):
    def build(self):
        self.layout = BoxLayout(orientation='vertical', padding=10, spacing=10)

        # إنشاء مربعات النص لإدخال القيم
        self.x11_input = TextInput(hint_text="Enter number (1,1)", multiline=False)
        self.x12_input = TextInput(hint_text="Enter number (1,2)", multiline=False)
        self.x13_input = TextInput(hint_text="Enter number (1,3)", multiline=False)
        self.x21_input = TextInput(hint_text="Enter number (2,1)", multiline=False)
        self.x22_input = TextInput(hint_text="Enter number (2,2)", multiline=False)
        self.x23_input = TextInput(hint_text="Enter number (2,3)", multiline=False)
        self.x31_input = TextInput(hint_text="Enter number (3,1)", multiline=False)
        self.x32_input = TextInput(hint_text="Enter number (3,2)", multiline=False)
        self.x33_input = TextInput(hint_text="Enter number (3,3)", multiline=False)

        # إنشاء زر لحساب المحددات
        self.calculate_button = Button(text="Calculate Determinant")
        self.calculate_button.bind(on_press=self.calculate_determinant)

        # إنشاء ليبل لعرض النتيجة
        self.result_label = Label(text="Result will be shown here")

        # إضافة العناصر إلى الواجهة
        self.layout.add_widget(self.x11_input)
        self.layout.add_widget(self.x12_input)
        self.layout.add_widget(self.x13_input)
        self.layout.add_widget(self.x21_input)
        self.layout.add_widget(self.x22_input)
        self.layout.add_widget(self.x23_input)
        self.layout.add_widget(self.x31_input)
        self.layout.add_widget(self.x32_input)
        self.layout.add_widget(self.x33_input)
        self.layout.add_widget(self.calculate_button)
        self.layout.add_widget(self.result_label)

        return self.layout

    def calculate_determinant(self, instance):
        try:
            # الحصول على القيم المدخلة من المستخدم
            x11 = float(self.x11_input.text)
            x12 = float(self.x12_input.text)
            x13 = float(self.x13_input.text)
            x21 = float(self.x21_input.text)
            x22 = float(self.x22_input.text)
            x23 = float(self.x23_input.text)
            x31 = float(self.x31_input.text)
            x32 = float(self.x32_input.text)
            x33 = float(self.x33_input.text)

            # حساب المحددات
            result = float(
                x11 * (x22 * x33 - x32 * x23) -
                x12 * (x21 * x33 - x31 * x23) +
                x13 * (x21 * x32 - x31 * x22)
            )

            # عرض النتيجة
            self.result_label.text = f"Determinant: {result}"
        except ValueError:
            self.result_label.text = "Please enter valid numbers!"

if __name__ == '__main__':
    DeterminantApp().run()
