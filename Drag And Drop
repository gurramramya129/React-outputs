import React, { useState } from 'react';

const DragAndDrop = () => {
  const [dragging, setDragging] = useState(false);

  const handleDragStart = (e) => {
    setDragging(true);
    e.dataTransfer.setData('text/plain', e.target.id);
  };

  const handleDragOver = (e) => {
    e.preventDefault();
  };

  const handleDrop = (e) => {
    e.preventDefault();
    const data = e.dataTransfer.getData('text/plain');
    const draggedItem = document.getElementById(data);
    draggedItem.style.display = 'block';
    e.target.appendChild(draggedItem);
    setDragging(false);
  };

  return (
    <div>
      <div
        id="dragItem"
        draggable
        onDragStart={handleDragStart}
        style={{
          width: '100px',
          height: '50px',
          backgroundColor: 'lightblue',
          border: '1px solid #ccc',
          textAlign: 'center',
          padding: '10px',
          margin: '5px',
          cursor: 'move',
          display: dragging ? 'none' : 'block',
        }}
      >
        Drag me
      </div>

      <div
        id="dropZone"
        onDragOver={handleDragOver}
        onDrop={handleDrop}
        style={{
          width: '300px',
          minHeight: '150px',
          border: '2px dashed #aaa',
          marginTop: '20px',
          padding: '10px',
        }}
      >
        Drop here
      </div>
    </div>
  );
};

export default DragAndDrop;
