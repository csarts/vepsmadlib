# MADLIBS FILE

import random

# VARIABLES

introlst = []

# 1
# noun = "."
# 2
# adjective = "."
# 3
# verbpt = "."
# 4 INACTIVE
# pron = "."
# 5
# place = "."
# 6
# thing = "."
# 7
# verbprt = "."
# 8
# verbft = "."
# 9 stuff like his
charpronoun = "."
# 4 stuff like he
charpronoun2 = "."
# | stuff like him
charpronoun3 = "."
# 0
names = ['John', 'Stacey', 'Martin', 'Lucy', 'Tommy']

# lord help me
sentence1 = ["0 wakes up in the morning, and the first thing 4 sees is 9 favorite poster, a poster of a 2 1.",
             "0 gets off 9 chair, and decides to do some homework after 7 for a few hours.",
             "0 walks into 9 room, looking for 9 6."]
sentence2 = ["\n0 begins 7 near 9 closet, and opens the door. 4 sees a 6.",
             "\n0 starts 7 near the window, but then trips and falls against 9 closet, opening it, and out falls a 6.",
             "\n4 looks at 9 window, seeing a 2 view of 5. Then, 4 goes to get 9 6, opening 9 closet door."]
sentence3 = ["\n4 looks down and sees a 2 6 near 9 feet.",
             "\n0 ignores a fallen item and looks for a 6. "
             "After searching unsuccessfully, 4 2ly picks up an item at 9 feet.",
             "\nAn item falls and hits | on the foot, and he 2ly yelps in pain."]
sentence4 = ["\n0 looks in astonishment at the item in 9 hands, which is a 2 6.",
             "\n4 2ly looks at the item, and throws it at a 5, breaking it.",
             "\n0 decides 4's hungry, and 2ly eats the item, and then starts 2 7 out of the room."]

# RANDOM THINGS

num1 = random.randint(1, 3)
num2 = random.randint(1, 5)
num3 = random.randint(1, 3)
num4 = random.randint(1, 3)
num5 = random.randint(1, 3)

# MOORE VARIABLES

# sentence 1
if num1 == 1:
    sentence = sentence1[0]
elif num1 == 2:
    sentence = sentence1[1]
else:
    sentence = sentence1[2]

# sentence 2
if num3 == 1:
    secondsentence = sentence2[0]
elif num3 == 2:
    secondsentence = sentence2[1]
else:
    secondsentence = sentence2[2]

# sentence 3
if num4 == 1:
    sentence3rd = sentence3[0]
elif num4 == 2:
    sentence3rd = sentence3[1]
else:
    sentence3rd = sentence3[2]

# sentence 4
if num5 == 1:
    sentence4th = sentence4[0]
elif num5 == 2:
    sentence4th = sentence4[1]
else:
    sentence4th = sentence4[2]

# random name
name = names[num2 - 1]

# gets pronouns
if (name == 'John') or (name == 'Martin') or (name == 'Tommy'):
    charpronoun = "his"
    charpronoun2 = "he"
    charpronoun3 = "him"
elif (name == 'Lucy') or (name == "Stacey"):
    charpronoun = "her"
    charpronoun2 = "she"
    charpronoun3 = "her"

# WELCOME MESSAGE

print("\nThis is the madlibs generator. Please type in an appropriate word next to each type of word shown on the "
      "screen. If you don't know what an adjective, noun, or anything else is, google it, you dummy. \n \n")

# REPLACES NAME AND PRONOUNS THIS IS CANCER I DONT KNOW WHY I DIDNT USE A NESTED FOR LOOP BUT ITS TOO LATE HAHAHAHAH
# I HAVE BRAIN DAMAGE

for i in sentence:
    if i == "0":
        sentence = sentence[:sentence.index(i, 0)] + name + sentence[sentence.index(i, 0) + 1:]
    elif i == "9":
        sentence = sentence[:sentence.index(i, 0)] + charpronoun + sentence[sentence.index(i, 0) + 1:]
    elif i == "4":
        sentence = sentence[:sentence.index(i, 0)] + charpronoun2 + sentence[sentence.index(i, 0) + 1:]
    elif i == "|":
        sentence = sentence[:sentence.index(i, 0)] + charpronoun3 + sentence[sentence.index(i, 0) + 1:]

for i in secondsentence:
    if i == "0":
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + name + secondsentence[
                                                                              secondsentence.index(i, 0) + 1:]
    elif i == "9":
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + charpronoun + secondsentence[
                                                                                     secondsentence.index(i, 0) + 1:]
    elif i == "4":
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + charpronoun2 + secondsentence[
                                                                                      secondsentence.index(i, 0) + 1:]
    elif i == "|":
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + charpronoun3 + secondsentence[
                                                                                      secondsentence.index(i, 0) + 1:]
for i in sentence3rd:
    if i == "0":
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + name + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "9":
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + charpronoun + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "4":
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + charpronoun2 + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "|":
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + charpronoun3 + sentence3rd[sentence3rd.index(i, 0) + 1:]

for i in sentence4th:
    if i == "0":
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + name + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "9":
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + charpronoun + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "4":
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + charpronoun2 + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "|":
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + charpronoun3 + sentence4th[sentence4th.index(i, 0) + 1:]

# GETS WORDS IN THE BEGINNING IF ANYONES READING THIS IM SO SO SO SORRY I DONT LIKE IT EITHER THIS IS SO BAD
# IVE ONLY BEEN REVIEWING PYTHON FOR A WEEK OKAY

for i in sentence:
    if i == "1":
        noun = input("Noun: ")
        # introlst.append(noun)
        sentence = sentence[:sentence.index(i, 0)] + noun + sentence[sentence.index(i, 0) + 1:]
    elif i == "2":
        adjective = input("Adjective: ")
        # introlst.append(adjective)
        sentence = sentence[:sentence.index(i, 0)] + adjective + sentence[sentence.index(i, 0) + 1:]
    elif i == "3":
        verbpt = input("Verb (past tense) [ex: ran]: ")
        # introlst.append(verbpt)
        sentence = sentence[:sentence.index(i, 0)] + verbpt + sentence[sentence.index(i, 0) + 1:]
    elif i == "5":
        place = input("Place: ")
        # introlst.append(place)
        sentence = sentence[:sentence.index(i, 0)] + place + sentence[sentence.index(i, 0) + 1:]
    elif i == "6":
        thing = input("Object: ")
        # introlst.append(thing)
        sentence = sentence[:sentence.index(i, 0)] + thing + sentence[sentence.index(i, 0) + 1:]
    elif i == "7":
        verbprt = input("Verb (present tense) [ex: running]: ")
        # introlst.append(verbprt)
        sentence = sentence[:sentence.index(i, 0)] + verbprt + sentence[sentence.index(i, 0) + 1:]
    elif i == "8":
        verbft = input("Verb (future tense) [ex: run (will run but without the will)]: ")
        # introlst.append(verbft)
        sentence = sentence[:sentence.index(i, 0)] + verbft + sentence[sentence.index(i, 0) + 1:]

for i in secondsentence:
    if i == "1":
        noun = input("Noun: ")
        # introlst.append(noun)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + noun + secondsentence[
                                                                              secondsentence.index(i, 0) + 1:]
    elif i == "2":
        adjective = input("Adjective: ")
        # introlst.append(adjective)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + adjective + secondsentence[
                                                                                   secondsentence.index(i, 0) + 1:]
    elif i == "3":
        verbpt = input("Verb (past tense) [ex: ran]: ")
        # introlst.append(verbpt)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + verbpt + secondsentence[
                                                                                secondsentence.index(i, 0) + 1:]
    elif i == "5":
        place = input("Place: ")
        # introlst.append(place)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + place + secondsentence[
                                                                               secondsentence.index(i, 0) + 1:]
    elif i == "6":
        thing = input("Object: ")
        # introlst.append(thing)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + thing + secondsentence[
                                                                               secondsentence.index(i, 0) + 1:]
    elif i == "7":
        verbprt = input("Verb (present tense) [ex: running]: ")
        # introlst.append(verbprt)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + verbprt + secondsentence[
                                                                                 secondsentence.index(i, 0) + 1:]
    elif i == "8":
        verbft = input("Verb (future tense) [ex: run (will run but without the will)]: ")
        # introlst.append(verbft)
        secondsentence = secondsentence[:secondsentence.index(i, 0)] + verbft + secondsentence[
                                                                                secondsentence.index(i, 0) + 1:]

for i in sentence3rd:
    if i == "1":
        noun = input("Noun: ")
        # introlst.append(noun)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + noun + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "2":
        adjective = input("Adjective: ")
        # introlst.append(adjective)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + adjective + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "3":
        verbpt = input("Verb (past tense) [ex: ran]: ")
        # introlst.append(verbpt)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + verbpt + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "5":
        place = input("Place: ")
        # introlst.append(place)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + place + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "6":
        thing = input("Object: ")
        # introlst.append(thing)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + thing + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "7":
        verbprt = input("Verb (present tense) [ex: running]: ")
        # introlst.append(verbprt)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + verbprt + sentence3rd[sentence3rd.index(i, 0) + 1:]
    elif i == "8":
        verbft = input("Verb (future tense) [ex: will run (but without the will)]: ")
        # introlst.append(verbft)
        sentence3rd = sentence3rd[:sentence3rd.index(i, 0)] + verbft + sentence3rd[sentence3rd.index(i, 0) + 1:]

for i in sentence4th:
    if i == "1":
        noun = input("Noun: ")
        # introlst.append(noun)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + noun + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "2":
        adjective = input("Adjective: ")
        # introlst.append(adjective)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + adjective + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "3":
        verbpt = input("Verb (past tense) [ex: ran]: ")
        # introlst.append(verbpt)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + verbpt + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "5":
        place = input("Place: ")
        # introlst.append(place)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + place + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "6":
        thing = input("Object: ")
        # introlst.append(thing)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + thing + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "7":
        verbprt = input("Verb (present tense) [ex: running]: ")
        # introlst.append(verbprt)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + verbprt + sentence4th[sentence4th.index(i, 0) + 1:]
    elif i == "8":
        verbft = input("Verb (future tense) [ex: run (will run but without the will)]: ")
        # introlst.append(verbft)
        sentence4th = sentence4th[:sentence4th.index(i, 0)] + verbft + sentence4th[sentence4th.index(i, 0) + 1:]

print("\n" + sentence + " " + secondsentence + " " + sentence3rd + " " + sentence4th)
