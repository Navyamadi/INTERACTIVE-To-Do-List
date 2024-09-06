document.addEventListener('DOMContentLoaded', () => {
    const taskInput = document.getElementById('taskInput');
    const addTaskButton = document.getElementById('addTaskButton');
    const taskList = document.getElementById('taskList');

    addTaskButton.addEventListener('click', () => {
        const taskText = taskInput.value.trim();
        if (taskText) {
            const li = document.createElement('li');
            li.innerHTML = `
                ${taskText} 
                <button class="deleteButton">Delete</button>
            `;
            taskList.appendChild(li);
            taskInput.value = '';

            const deleteButton = li.querySelector('.deleteButton');
            deleteButton.addEventListener('click', () => {
                taskList.removeChild(li);
            });
        }
    });

    taskInput.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') {
            addTaskButton.click();
        }
    });
});
