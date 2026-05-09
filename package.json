const { contextBridge, ipcRenderer } = require('electron');

contextBridge.exposeInMainWorld('electronAPI', {
    readModule: (modulePath) => ipcRenderer.invoke('read-module', modulePath),
    selectFiles: () => ipcRenderer.invoke('select-files'),
    createDatabase: (fileName) => ipcRenderer.invoke('create-database', fileName),
    saveDatabaseFile: (fileName, data) => ipcRenderer.invoke('save-database-file', fileName, data)
});
