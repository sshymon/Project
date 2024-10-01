# Simple To-Do List Application in Python

class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append({"task": task, "done": False})
        print(f"Task '{task}' has been added.")

    def remove_task(self, task_index):
        if 0 <= task_index < len(self.tasks):
            removed_task = self.tasks.pop(task_index)
            print(f"Task '{removed_task['task']}' has been removed.")
        else:
            print("Invalid task number.")

    def mark_task_as_done(self, task_index):
        if 0 <= task_index < len(self.tasks):
            self.tasks[task_index]["done"] = True
            print(f"Task '{self.tasks[task_index]['task']}' has been marked as done.")
        else:
            print("Invalid task number.")

    def show_tasks(self):
        if not self.tasks:
            print("No tasks to show.")
        else:
            for idx, task in enumerate(self.tasks):
                status = "done" if task["done"] else "not done"
                print(f"{idx + 1}. {task['task']} [{status}]")

def main():
    todo_list = ToDoList()
    while True:
        print("\n1. Add a task")
        print("2. Remove a task")
        print("3. Mark task as done")
        print("4. Show tasks")
        print("5. Exit")

        choice = input("Choose an option (1-5): ")

        if choice == "1":
            task = input("Enter the task: ")
            todo_list.add_task(task)
        elif choice == "2":
            todo_list.show_tasks()
            task_num = int(input("Enter the task number to remove: ")) - 1
            todo_list.remove_task(task_num)
        elif choice == "3":
            todo_list.show_tasks()
            task_num = int(input("Enter the task number to mark as done: ")) - 1
            todo_list.mark_task_as_done(task_num)
        elif choice == "4":
            todo_list.show_tasks()
        elif choice == "5":
            print("Exiting the application. Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
