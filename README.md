# <p align="center"> Roll a Ball</p>

## Aim:
To Roll a Ball using C# program in unity .
## Algorithm:
### Step 1:
Create New Scene on unity game engine.

### Step 2:
Right click on Hierarchy create 3D Object.

### Step 3:
Click Hierarchy -> 3DObject -> Sphere Hierarchy -> 3DObject -> plane Hierarchy.

### Step 4:
Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Cylinder to the plane and release the mouse

Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Plane) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Capsule to the plane and release the mouse

### Step 5:
Create a folder name Coding and create a C# file to add the coding in it.

### Step 6:
To add our C# Script file to our selected object, click on the C# Script file and drag it to Sphere objects in the Hierarchy window and run the application.

### Step 7:
After run the application, you press the WASD and space key the ball will move and jump.
## Program:
```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class movement : MonoBehaviour
{
    public float xforce=5.0f,yforce=150.0f,zforce=5.0f;
    // Start is called before the first frame update
    void Start()
    {
        
    }
    // Update is called once per frame
    void Update()
    {
        float x=0.0f,y=0.0f,z=0.0f;
        if(Input.GetKey(KeyCode.A))
        {
            x=x-xforce;
        }
        if(Input.GetKey(KeyCode.W))
        {
            z=z+zforce;
        }
        if(Input.GetKey(KeyCode.D))
        {
            x=x+xforce;
        }
        if(Input.GetKey(KeyCode.S))
        {
            z=z-zforce;
        }
        if(Input.GetKey(KeyCode.Space))
        {
            y=yforce;
        }
        GetComponent<Rigidbody>().AddForce(x,y,z);
    }
}
```
## Output:
![Screenshot (6)](https://user-images.githubusercontent.com/75234646/190055040-cc56a875-9f54-40e5-bbd9-028e2c3f0391.png)


## Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
