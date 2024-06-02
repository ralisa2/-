Python. 
 
import os 
from docx import Document 
 
def generate_statement(student_name, courses): 
    doc = Document() 
    doc.add_heading('Заявление на выбор факультативов и дисциплин по выбору', level=1) 
     
    doc.add_paragraph(f'Я, {student_name}, прошу зачислить меня на следующие курсы:') 
     
    for course in courses: 
        doc.add_paragraph(f'- {course}') 
         
    doc.add_paragraph('С уважением,') 
    doc.add_paragraph(student_name) 
     
    doc.save(f'{student_name}_заявление.docx') 
 
student_name = 'Иванов Иван' 
courses = ['Математика', 'Литература', 'Искусство'] 
generate_statement(student_name, courses)
