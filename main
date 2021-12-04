import random

print('Enter the number of friends joining (including you):')
num = int(input())

try:
	assert num > 0, 'No one is joining for the party'
	print('Enter the name of every friend (including you), each on a new line:')
	list_name = [input() for _ in range(num)]
	dict_name = dict.fromkeys(list_name, 0)
	print('\nEnter the total bill value:')
	summ = int(input())
	num_people = len(dict_name)

	print('Do you want to use the "Who is lucky?" feature? Write Yes/No:')
	answer = input()
	lucky = ''
	if answer == 'Yes':
		lucky = random.choice(list(dict_name.keys()))
		print()
		print(lucky, 'is the lucky one!')
		num_people -= 1
	else:
		print('No one is going to be lucky')

	share = round(summ / num_people, 2)
	for key in dict_name:
		if key == lucky:
			dict_name[lucky] = 0
		else:
			dict_name[key] = share
	print(dict_name)
except Exception:
	print("No one is joining for the party")
