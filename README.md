questions = [
    [
        "who are the five members of un committe  ?", "china , israel , russia , the united states and united kingdom", "China, France, Russia, Netherland, and the United States.", "China, France, russia, canada, and the United States.",
        "China,france  , Russia, the United Kingdom, and the United States.", "None", 4
    ],
    [
        "when was crips mission held in terms of years ?", "1943", "1944", "1946",
        "1942", "None", 4

    ],
    [
        "when was cabinet mission held in terms of years ?", "1940", "1945", "1942",
        "1946", "None", 4
    ],
    [
        "who was the chairmen of committee on fundamental rights ?", "mahtma gandhi ", "rajendra parsad ", "Br ambedkar",
        "vallabhai patel ", "None", 4
    ],
    [
        "who was the chairmen of finance of staff committe ?", "vallabhai patel ", "alladi krishna ", "A.V Thakkar",
        "Rajendra parsad ", "None", 4
    ],
    [
        "constitution of india was adopted buy the constituent assembly on ?", "22 Nov 1948", "23 Nov 1949", "26 Nov 1948",
        "26 Nov 1949", "None", 4
    ],
    [
        "the union territories  atricles terms  ?", "238-240", "239-243", "239-245",
        "239-242", "None", 4
    ],
    [
        "indian army day is celebrated on which day?", "12 january", "13 january ", "16 january ",
        "15 january ", "None", 4
    ],
]
levels = [1000, 2000, 3000, 4000, 5000, 6000, 7000, 8000, 9000, 10000,
          12000, 14000, 16000, 18000, 20000, 22000, 25000, 28000, 30000, 32000,]
money = 0
for i in range(0, len(questions)):
    question = questions[i]
    print(f"question for RS. {levels[i]}\n")
    print(f" {question[0]}\n a. {question[1]}                          b. {question[2]}                  c. {question[3]}                    d. {question[4]}")
    reply = int(input("Enter your answer (a-d) or  0 to quit:\n"))
    if (reply == 0):
        money = levels[i-1]
        break
    if (reply == question[-1]):
        print(f"correct answer,you have won {levels[i]}")
        if (i == 4):
            money = 5000
        elif (i == 8):
            money = 8000
        elif (i == 12):
            money = 16000
    else:
        print("wrong answer")
        break
print(f"your take home money is {money}")
