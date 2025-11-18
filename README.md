# Kanban Todo App

A modern, project-based Kanban todo list application built with React, featuring markdown export and a unique card view for managing multiple projects.

![Kanban Todo App](https://img.shields.io/badge/React-18.2.0-blue)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.3.0-green)
![Vite](https://img.shields.io/badge/Vite-4.4.5-purple)

## Features

- 🎯 **Project-Based Organization**: Create and manage multiple independent projects
- 📋 **Kanban Board**: Classic three-column layout (To Do, In Progress, Done)
- 🗂️ **Card View**: Unique corner-positioned project overview
- 📅 **Date Tracking**: Automatic timestamps and day counters for all tasks
- 📝 **Markdown Export**: Export projects to properly formatted markdown files
- 💾 **Data Persistence**: Automatic saving to browser localStorage
- 🎨 **Modern UI**: Clean, responsive design with Tailwind CSS

### Task Format Example
```markdown
* [ ] task 1 {Mon. 17 Nov 2025} 1 day
* [x] completed task {Sun. 16 Nov 2025} 2 days
```

## Quick Start

### Option 1: Run Locally

#### Prerequisites
- [Node.js](https://nodejs.org/) (version 16 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

#### Installation Steps

1. **Download and extract** all the files to a folder on your computer

2. **Open terminal/command prompt** in that folder

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Start the development server**:
   ```bash
   npm run dev
   ```

5. **Open your browser** and visit: `http://localhost:5173`

That's it! Your Kanban app is now running locally.

#### Additional Commands
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally

### Option 2: Deploy to GitHub Pages (Free Hosting)

#### Step-by-Step GitHub Deployment

1. **Create a new repository** on GitHub:
   - Go to [github.com](https://github.com) and sign in
   - Click "New repository"
   - Name it `kanban-todo-app` (or any name you prefer)
   - Make it **Public** (required for free GitHub Pages)
   - Click "Create repository"

2. **Upload your files**:
   - Download all the files from this project
   - In your new GitHub repository, click "uploading an existing file"
   - Drag and drop all the files (keep the folder structure intact)
   - Commit the files with message "Initial commit"

3. **Enable GitHub Pages**:
   - In your repository, go to **Settings** tab
   - Scroll down to **Pages** section (in the left sidebar)
   - Under **Source**, select "GitHub Actions"
   - The workflow will automatically trigger

4. **Access your website**:
   - After 2-3 minutes, your site will be available at:
   - `https://yourusername.github.io/kanban-todo-app/`

#### Alternative: Manual Upload Method

If you prefer not to use git commands:

1. Download all project files
2. Visit your GitHub repository
3. Click "Add file" → "Upload files"
4. Drag all files maintaining the folder structure
5. Commit changes
6. Enable GitHub Pages as described above

## Project Structure

```
kanban-todo-app/
├── src/
│   ├── KanbanTodoApp.jsx    # Main React component
│   ├── main.jsx             # React entry point
│   └── index.css            # Tailwind CSS styles
├── .github/
│   └── workflows/
│       └── deploy.yml       # GitHub Actions workflow
├── index.html               # HTML template
├── package.json             # Dependencies and scripts
├── vite.config.js           # Vite configuration
├── tailwind.config.js       # Tailwind CSS configuration
└── postcss.config.js        # PostCSS configuration
```

## How to Use

### Basic Usage
1. **Create tasks**: Type in the input field and click "Add Task"
2. **Move tasks**: Use the colored buttons to move tasks between columns
3. **Create projects**: Use "Add Project" to create new project boards
4. **Switch projects**: Use the dropdown to change between projects

### Card View
1. Click "Card View" to see all projects at once
2. Projects appear in screen corners (top-left, top-right, bottom-left, bottom-right)
3. Click "Open Project" on any card to switch to that project
4. Click "Close Card View" to return to normal view

### Markdown Export
1. Click "Export as Markdown" to download your current project
2. Files are saved with proper markdown formatting
3. Includes all task details with timestamps and day counters

## Customization

### Changing Colors
Edit `src/KanbanTodoApp.jsx` and modify the Tailwind classes:
- `bg-blue-500` for blue backgrounds
- `bg-green-500` for green backgrounds
- `text-gray-700` for text colors

### Adding Features
The code is well-structured and commented. Key areas:
- Task management: Functions like `addTask`, `moveTask`, `deleteTask`
- Project management: `addProject`, `deleteProject`
- UI components: `ProjectCard` component for the card view

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Data Storage

- All data is stored in your browser's localStorage
- Data persists between sessions
- No server or database required
- Export to markdown for backups

## Contributing

Feel free to fork this project and submit pull requests for improvements!

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Troubleshooting

**Port already in use?**
```bash
npm run dev -- --port 3001
```

**Build fails?**
```bash
rm -rf node_modules package-lock.json
npm install
npm run build
```

**GitHub Pages not working?**
- Make sure repository is public
- Check GitHub Actions tab for error messages
- Wait 5-10 minutes for changes to propagate

---

Made with ❤️ using React, Vite, and Tailwind CSS
