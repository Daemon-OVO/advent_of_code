# "/aoc_day1_input.txt"
def day_1(input_file):
  # open file
  with open(input_file) as data_input:
    # remove all new line breaks from the end of each record
    strip_file = [line.rstrip('\n') for line in data_input.readlines()]
    # Create a dictionary that will assign a number to an elf and their sum total calories.
    elf_book = {}
    # assign a number to each elf's inventory
    elf_number  = -1
    # set a default value of 0 to start summing inventory calories
    calories_sum = 0
    for record in strip_file:
        if record == '':
              # when a lines value is empty assign the total calorie sum to the elf and then reset the sum
              elf_number += 1
              elf_book[elf_number] = calories_sum
              calories_sum = 0
        else:
          # sum until an empty value is identified.
          calories_sum += int(record)
  return elf_book


def day_1_results(dictionary):
  # idenitfy elf with the most calories
  greediest_elf = max(dictionary, key=dictionary.get)
  greediest_elf_calories = dictionary[greediest_elf]
  # f"{}"
  part_1 = print(f"elf {greediest_elf} holds the most calories at: {greediest_elf_calories}")
  # Find the top three Elves carrying the most Calories. Sum total Calories those Elves are carrying
  top_3 = sorted(dictionary, key=dictionary.get, reverse=True)[:3]
  top_3_calories = [dictionary[elf] for elf in top_3]
  part_2 = print("elves {} hold the most calories at: {} for a total of: {}".format(top_3, top_3_calories, sum(top_3_calories)))


def output():
  answ1 = day_1("aoc_day1_input.txt")
  answ2 = day_1_results(answ1)
  print(answ2)


output()
