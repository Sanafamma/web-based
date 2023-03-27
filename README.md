# web-based
from flask import Flask, request, jsonify

app = Flask(__web__)

# No authentication or authorization implemented
# No data encryption or input validation implemented

@app.route('/project', methods=['POST'])
def create_project():
    data = request.get_json()
    title = data['title']
    description = data['description']
    deadline = data['deadline']

    # save project to database

    return jsonify({'message': 'Project created successfully.'}), 201

@app.route('/task', methods=['POST'])
def create_task():
    data = request.get_json()
    title = data['title']
    description = data['description']
    deadline = data['deadline']
    project_id = data['project_id']
    assigned_to = data['assigned_to']
    priority = data['priority']

    # save task to database

    return jsonify({'message': 'Task created successfully.'}), 201
