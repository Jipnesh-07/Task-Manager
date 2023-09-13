# Task-Manager
This code is a JavaScript implementation of a web application for managing a to-do list. It allows users to add, edit, delete, and search for tasks. The application uses HTML and CSS for the structure and styling, and JavaScript for the functionality. I'll explain the code in detail section by section:

1. **Element Selection and Initialization**:
   - The code begins by selecting various HTML elements using the `document.querySelector` method. These elements include the task input field (`task_input`), date input field (`date_input`), add button (`add_btn`), list body for displaying tasks (`todos_list_body`), alert message container (`alert_message`), and a delete all button (`delete_all_btn`).
   - It initializes an array named `todos` which will hold the tasks. It loads tasks from local storage if they exist, or initializes an empty array if not.

2. **Window Load Event Listener**:
   - When the DOM content is loaded, a function is executed.
   - The function calls `showAllTodos()` to display the tasks.
   - If there are no tasks, it displays a message in the list body.

3. **Generating a Random Unique ID**:
   - The `getRandomId()` function generates a random alphanumeric ID for each task. It's used to uniquely identify tasks.

4. **Adding a Task**:
   - The `addToDo()` function creates a task object with properties like `id`, `task`, `dueDate`, `completed`, and `status`.
   - The `task` and `dueDate` are extracted from the input fields.
   - The task object is pushed into the `todos` array.

5. **Event Listeners for Adding Tasks**:
   - The code adds event listeners for the "Enter" key press in the task input field (`task_input`), and for the click of the add button (`add_btn`).
   - When the "Enter" key is pressed and the input field is not empty, a task is added.
   - When the add button is clicked, if the input field is not empty, a task is added and an alert message is displayed.

6. **Clearing All Tasks**:
   - The `clearAllTodos()` function is called when the delete all button is clicked.
   - It clears all tasks from the `todos` array and updates local storage.

7. **Displaying Tasks**:
   - The `showAllTodos()` function displays all tasks in the list body.
   - If no tasks are present, a message is displayed.
   - It iterates through the `todos` array and generates HTML elements for each task, including buttons for editing, toggling status, and deleting.

8. **Deleting a Task**:
   - The `deleteTodo(id)` function removes a task from the `todos` array by filtering out the task with the provided ID.
   - It also updates local storage and displays an alert message.

9. **Editing a Task**:
   - The `editTodo(id)` function allows editing a task by setting the task input field with the task's content.
   - When the edit is confirmed, the task is updated in the `todos` array, and an alert message is shown.

10. **Toggling Task Status**:
    - The `toggleStatus(id)` function changes the completion status of a task when the status button is clicked.
    - It updates the task's `completed` and `status` properties, saves to local storage, and updates the display.

11. **Searching for Tasks**:
    - The `searchInput` element is an input field where users can enter a search term.
    - The `handleSearch()` function filters tasks based on the search term and updates the display.

12. **Voice Search**:
    - The voice search feature lets users search by speaking into their microphone.
    - It uses the `webkitSpeechRecognition` API to capture spoken input.
    - The `voiceSearchButton` triggers the voice recognition.
    - The `recognition.onresult` event captures the voice result, updates the search input, and performs a search.

13. **Filtering Tasks by Status**:
    - The `filterTodos(status)` function allows users to filter tasks by "all", "pending", or "completed" status.
    - It updates the display based on the selected filter.

14. **Displaying Filtered Tasks**:
    - The `displayTodos(todosArray)` function updates the list body with the provided array of tasks.
    - It generates HTML elements for each task in the array.

Overall, this code creates a functional to-do list application with features like adding, editing, deleting, searching, and filtering tasks. It also incorporates a voice search feature using the SpeechRecognition API.
