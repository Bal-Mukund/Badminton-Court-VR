
# Badminton Court VR

A Virtual Replica of the Badminton Court made with Unity 3D Game Engine, the VR replica gives the realistic experience of the Badminton Court to its users. In this replica users don't have to move physically to move in the virtual world, users just have to move their heads below 30 degrees to move in that particular direction.

Through the use of Virtual Reality (VR) technology, users can explore and interact with the virtual environment in a way that closely mimics real-life. The project is compatible with Google Cardboard and other popular VR headsets, allowing users to experience the virtual world in a way that suits them best.

The Virtual Badminton Court project uses cutting-edge VR technology to allow users to move through the virtual environment without having to move in the real world. Users can explore the virtual badminton court by simply moving their head within a 30-degree range. This makes it incredibly easy for users to move around the court.

Overall, the Virtual Badminton Court project is a prime example of how VR technology can be used to create a highly immersive and engaging experience for users. Whether you're a badminton enthusiast or just looking for a fun and interactive way to explore a virtual environment, this project is sure to provide an realistic experience.




## Features

- **Virtual replica of a badminton court:** The project provides an accurate virtual replica of a badminton court, allowing users to experience the court in a fully immersive way.

- **VR compatibility:** The project is compatible with Google Cardboard and other popular VR headsets, providing users with an incredibly immersive experience.

- **Non-physical movement:** Users can move through the virtual environment without having to move in the real world, making it a convenient and easy way to explore the virtual badminton court by simply moving their head within a 30-degree range.

-  **Multi-device compatibility:** The project has been extensively tested to ensure compatibility with a range of devices and VR headsets, making it easily accessible to users.

-  **Convenient and engaging:** The Virtual Badminton Court project provides users with a convenient and engaging way to experience a badminton court in a virtual environment.

- **User-friendly navigation:** Clear instructions are provided to ensure that users can easily navigate and explore the virtual environment.



## Screenshots

![App Screenshot](c:\Users\balmu\Downloads\Badminton Court Screenshot 01.png)

![App Screenshot](c:\Users\balmu\Downloads\Badminton Court Screenshot.png)

## C# Scripting

_ **
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class VRLookWalk : MonoBehaviour
{

    public Transform vrCamera;
    public float toggleAngle = 30.0f;
    public float speed = 3.0f;
    public bool moveForward;

    private CharacterController cc;

    // Use this for initialization
    void Start()
    {
        cc = GetComponent<CharacterController>();
    }

    // Update is called once per frame
    void Update()
    {
        if (vrCamera.eulerAngles.x >= toggleAngle && vrCamera.eulerAngles.x < 90.0f)
        {
            moveForward = true;
        }
        else
        {
            moveForward = false;
        }

        if (moveForward)
        {
            Vector3 forward = vrCamera.TransformDirection(Vector3.forward);

            cc.SimpleMove(forward * speed);
        }
    }
}**



