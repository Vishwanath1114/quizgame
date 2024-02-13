print("Welcome to Quiz Game")


question_bank=[
    {"text":"The ability of one class to acquire methods   and attritubes  from another class is called?","answer":"A"},
    {"text":"what type of  inheritance has multiple subclasses to a single superclass?","answer":"c"},
    {"text":"which of the following is a type of inheritance?","answer":"D"},
    {"text":"what does MRO stand for?","answer":"B"}  
    
]

options=[["A.Inheritance","B.Abstraction","C.Polymorphism","D.objects"],
         ["A.Multiple inheritance","B.Multilevel inheritance","C.Hierarchical inheritance","D.None of these"],
         ["A.Single","B.Double","C.Multiple","D.Both A and B"],
         ["A.Method recursive object","B.Method resolution order","C.Main resolution order","D.Method resolution object"]
         
]

score=0
def check_answer(user_guess,correct_answer):
    if user_guess==correct_answer:
        return True
    else:
        return False
for question_num in range(len(question_bank)):# 0 1 2 3 
    print("------------------------------")
    print(question_bank[question_num]["text"])
    
    for i in options[question_num]:
        print(i)
    
    
    guess=input("Enter your answer(A/B/C/D):").upper()
    is_correct=check_answer(guess,question_bank[question_num]["answer"])  
    if is_correct:
        print("Correct Answer")
        score +=1  
    else:
        print("Incorrect Answer")
        print(f"the correct answer is {question_bank[question_num]['answer']}")
        print(f"your current score is {score}/{question_num+1}")

print(f"You have given {score}correct answer")
print(f"your score is {(score/len(question_bank))*100}%")
        
