# winer_generator
from PyQt5.QtCore import *
from PyQt5.QtWidgets import *
from random import randint
def generate():
    n = randint(1,100)
    text.setText("Переможець")
    number.setText(str(n))
dodatok = QApplication([])
win= QWidget()
win.resize(400,200)
win.move(100,100)
win.setWindowTitle("Генератор переможця")
text = QLabel('Натисни, щоб дізнатися переможця')
number = QLabel("?")
button= QPushButton('Зенерувати')
line = QVBoxLayout()
line.addWidget(text,alignment=Qt.AlignCenter)
line.addWidget(number,alignment=Qt.AlignCenter)
line.addWidget(button,alignment=Qt.AlignCenter)
win.setLayout(line)
button.clicked.connect(generate)
win.show()
dodatok.exec()
