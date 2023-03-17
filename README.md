# laundry
# list of laundry tasks by mama fuas
laundry_tasks = ['Wash whites', 'Wash darks', 'Dry clothes', 'Fold clothes']

# define a list of mama fuas who will do the laundry
mama_fua = ['Alice', 'Bob', 'Charlie', 'Dave']

#  how many tasks each mama fua will do
tasks_per_mama_fua = len(laundry_tasks) // len(mama_fua)

#task assigning to mama fuas
laundry_allocation = {}
for i, task in enumerate(laundry_tasks):
    person_index = i % len(mama_fua)
    person = mama_fua[person_index]
    if person in laundry_allocation:
        laundry_allocation[person].append(task)
    else:
        laundry_allocation[person] = [task]

# laundry allocation printing
for person, tasks in laundry_allocation.items():
    print(f"{person} will do {len(tasks)} tasks:")
    for task in tasks:
        print(f"\t{task}")
