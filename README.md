# 🛠️ MANUFAI_freecad_plugin
### Advanced Welding Engineering & Simulation Workbench

**MANUFAI** is a specialized workbench developed for **FreeCAD**, engineered to bridge the critical gap between static 3D CAD design and dynamic manufacturing processes. It transforms standard geometry into actionable, simulatable welding plans without leaving the design environment.

The core philosophy of this plugin is to streamline the transition from a digital design to a physical application. By analyzing 3D models, the workbench allows users to define, optimize, and export welding paths with a level of detail typically reserved for high-end proprietary software. It is not just about drawing lines; it is about assigning manufacturing logic to geometry.

#### **Key Capabilities:**
* **Intelligent Geometry Analysis:** The system can scan a 3D model to automatically extract edges, specifically identifying weldable candidates such as **90-degree unions** or T-joints, significantly reducing manual selection time.
* **Versatile Path Generation:** Users have total control over how weld beads are generated. Options include creating continuous weld lines, applying specific **offsets** from the edge, or generating **intermittent (stitch) welds** based on structural requirements.
* **Technical Definition:** Beyond geometry, the plugin calculates surface normals to ensure correct torch orientation and assigns specific material properties to the weld lines for accurate cost and thermal analysis.
* **Process Simulation & Sequencing:** It allows engineers to simulate the execution of the welding process—whether performed by a robot or a human operator. Users can define the **welding sequence** (order of operations) to minimize thermal distortion and calculate precise cycle times.
* **Comprehensive Reporting:** The workbench automatically generates detailed engineering reports, providing critical data such as total weld length, estimated material consumption, and operation times.

---

### 🌐 Interoperability: From CAD to Reality
We understand that FreeCAD is often just one part of a larger industrial ecosystem. Therefore, **MANUFAI** is designed to act as a bridge to advanced simulation and CAM solutions.

We have expanded the plugin’s core functionality to ensure seamless connectivity with industry-standard software like **RoboDK**, **C3P**, and other solvers. This allows users to export their defined welding paths and process data directly into professional simulation environments, validating kinematics and physics before the project ever reaches the factory floor.

---

## 🚀 New Feature Highlights

<table>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Recursive%20Visibility/Toggle_Visibility_Recursive.svg" width="100px">
    </td>
    <td>
      <h3>Recursive Visibility Toggle</h3>
      <strong>Instantly restore visual control over complex assemblies.</strong>
      <br><br>
      The <strong>Recursive Visibility</strong> tool solves UX friction when working with complex hierarchies. It traverses the entire dependency tree of a selected object to toggle visibility for the parent and all descendants recursively.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/0fa2cd8d-c080-43f4-a0a1-9e60bd4e93ff" width="100%" controls></video>
    </td>
  </tr>
</table>

## 📏 3-2-1 Alignment

<table>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Create%20Sphere%20in%20Origin/ORIGEN.svg" width="100px">
    </td>
    <td>
      <h3>Create Sphere in Origin</h3>
      <strong>Generates a visual reference at the Global Origin (0,0,0).</strong>
      <br><br>
      It places a reference sphere at the absolute zero of the workspace. This provides an immediate visual check to determine the offset distance of imported models relative to the workspace center before starting any alignment procedures.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/3d7e01eb-258b-4d20-ac01-b414544c3b89" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Create%20Center%20Point/CENTRO.svg" width="100px">
    </td>
    <td>
      <h3>Create Center Point</h3>
      <strong>Calculates geometric centers for quick referencing.</strong>
      <br><br>
      It computes and marks the center point based on the current selection.
      <ul>
        <li><strong>Single Object:</strong> Marks the center of mass/geometry.</li>
        <li><strong>Two Objects:</strong> Calculates the exact midpoint between them.</li>
      </ul>
      Useful for establishing auxiliary reference points on complex geometry without creating full datums.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/417329b5-e28c-4d58-a506-29fc3a2ab8fc" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Datum%20A/DATUM_A.svg" width="100px">
    </td>
    <td>
      <h3>Datum A</h3>
      <strong>Defines the Primary Reference (Z-Axis / Plane).</strong>
      <br><br>
      It establishes the main orientation plane, locking 3 degrees of freedom. It features <strong>intelligent geometry recognition</strong>:
      <ul>
        <li><strong>Face Selection:</strong> Uses the normal of a flat face.</li>
        <li><strong>Dual-Edge Selection:</strong> By selecting two edges (e.g., two holes) sequentially, it computes the centerline between them to act as the primary axis.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/66e3217b-d3d2-4cce-bee3-ef0f11afa07d" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Datum%20B/DATUM_B.svg" width="100px">
    </td>
    <td>
      <h3>Datum B</h3>
      <strong>Defines the Secondary Reference (X-Axis / Direction).</strong>
      <br><br>
      It establishes the directional axis, locking 2 degrees of freedom. It includes a <strong>Virtual Midplane</strong> function:
      <ul>
        <li><strong>Edge/Face:</strong> Uses standard edges or faces for direction.</li>
        <li><strong>Extension Plane:</strong> When two parallel faces are selected, it calculates the theoretical mid-plane between them to define the axis.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/4afad79e-905f-4ac8-a5fe-194b80d1ab69" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Datum%20C/DATUM_C.svg" width="100px">
    </td>
    <td>
      <h3>Datum C</h3>
      <strong>Defines the Tertiary Reference (Exact Origin Point).</strong>
      <br><br>
      It locks the final degree of freedom, establishing the specific zero point along the previously defined axes. It accepts vertices, sphere centers, or calculates the midpoint between two selected edges/features.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/99ba5a36-2ca3-4c6e-80b7-b5580b0e3371" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Alignment%203-2-1/ALINEACION.svg" width="100px">
    </td>
    <td>
      <h3>Alignment 3-2-1</h3>
      <strong>Computes the coordinate system and previews the result.</strong>
      <br><br>
      It launches the Alignment Wizard to process the defined Datums (A, B, and C). It mathematically computes the orthogonal intersection of the vectors and displays a <strong>ghost preview</strong> of the new coordinate system, allowing validation of the new origin position before any actual movement occurs.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/8d0606ab-7623-448c-b674-eaebb61a4d86" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Move%20to%20Origin%203-2-1/MOVER.svg" width="100px">
    </td>
    <td>
      <h3>Move to Origin 3-2-1</h3>
      <strong>Executes the physical transformation (Assembly Safe).</strong>
      <br><br>
      It applies the calculated inverse transformation matrix to the selected objects, moving the model to the absolute (0,0,0).
      <br><strong>Hierarchy Awareness:</strong> It respects the document structure, moving parent containers or individual parts correctly without breaking internal assembly relationships or positions.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/bca2b1cf-31c2-4d74-ac5b-55ccedcbefaf" width="100%" controls></video>
    </td>
  </tr>
</table>

## 📊 Data Management

<table>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Find%20Data/DATA_ICON.svg" width="100px">
    </td>
    <td>
      <h3>Find Data Panel</h3>
      <strong>Centralized control for weld tracking and interoperability.</strong>
      <br><br>
      This tool opens a dedicated side panel that automatically scans the active document to identify and list all generated <strong>Weld Objects</strong>. It serves as the bridge between FreeCAD and external collaborators.
      <br><br>
      <strong>Key Features:</strong>
      <ul>
        <li><strong>Instant Detection:</strong> Click to locate and highlight specific weld beads in the 3D view immediately.</li>
        <li><strong>Flexible Data Export:</strong> Generates a <code>.txt</code> report of the selected welds to share with other departments or software. It offers two modes:
          <ul>
            <li><strong>Simple Report:</strong> Exports essential identification, coordinates, and basic geometry data.</li>
            <li><strong>Detailed Dump:</strong> Exports <strong>every single internal property</strong> stored by FreeCAD for that object. This "Full-Dump" mode is ideal for deep debugging or when external solvers need access to raw parametric data without opening the CAD file.</li>
          </ul>
        </li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/8bcf2251-f0bc-42cd-95bf-08ef1ecd7db7" width="100%" controls></video>
    </td>
  </tr>
</table>

## ⚡ Welding & Process Management Tools

<table>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Line%20Weld/weld_icon.svg" width="100px">
    </td>
    <td>
      <h3>Line Weld (Main Interface)</h3>
      <strong>Initializes the Workbench Core.</strong>
      <br><br>
      This is the <strong>master switch</strong> of the plugin. It must be active for all other welding tools to function correctly.
      <ul>
        <li><strong>Property Injection:</strong> Automatically recognizes drawn lines and injects necessary welding properties (Sequence, Layer, Electrical parameters).</li>
        <li><strong>System Activation:</strong> Launches the sidebar dock that manages the active welding context.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/ac970131-a3a0-4683-87e5-b3279ccc3fa8" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Line%20Weld%20Table/table_icon.svg" width="100px">
    </td>
    <td>
      <h3>Line Weld Table</h3>
      <strong>Parameter Editor & WDCurve Exporter.</strong>
      <br><br>
      Opens a comprehensive table interface to view and edit the technical data of every weld line in the document. It serves as the final step in the workflow.
      <ul>
        <li><strong>Bulk Editing:</strong> Modify Voltage (U), Current (I), Speed (V), and Sequence for multiple lines at once.</li>
        <li><strong>Drag-and-Drop Sequencing:</strong> Reorder the welding sequence visually.</li>
        <li><strong>Simultaneous Ops:</strong> Define which welds are executed in parallel by different robots.</li>
        <li><strong>Final Export:</strong> Once layers, sequences, and custom data are fully defined, this tool is responsible for <strong>generating the .WDCurve file</strong>, exporting only the active layers ready for external processing.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/d2e4cd18-238f-4066-9d3a-60538c8d200d" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/fa315d8f0b63aa7812cf4790a741954dbfa776bf/Selection%20Mode/selection_mode.svg" width="100px">
    </td>
    <td>
      <h3>Selection Mode (X-Ray & Filter)</h3>
      <strong>Visual isolation and Selection Lock.</strong>
      <br><br>
      A specialized view mode designed for working in complex assemblies.
      <ul>
        <li><strong>X-Ray Vision:</strong> Makes the 3D geometry transparent while keeping weld lines solid and visible.</li>
        <li><strong>Click-Through Blocker:</strong> <strong>Crucial Feature.</strong> It strictly blocks the selection of 3D geometry (faces/bodies), ensuring that clicks <strong>only register on weld lines</strong>. This prevents accidental selection of the background model when picking thin weld paths.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/a1e57451-0914-438f-9c8f-d2096a48de29" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Assign%20Layer/layer_icon.svg" width="100px">
    </td>
    <td>
      <h3>Assign Layer</h3>
      <strong>Advanced Grouping for Parts & Welds.</strong>
      <br><br>
      Beyond simple tagging, this tool creates logical containers (Layers) that can hold both <strong>weld paths</strong> and <strong>3D geometry parts</strong>.
      <ul>
        <li><strong>Context grouping:</strong> Associate specific fixtures or parts with a weld layer.</li>
        <li><strong>Preparation for View:</strong> This grouping structure is required to utilize the advanced filtering capabilities of the Visibility Manager.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/5e558c9f-b530-416a-bd68-8e8d0b686aa7" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Visibility%20Manager/visibility_icon.svg" width="100px">
    </td>
    <td>
      <h3>Visibility Manager (View)</h3>
      <strong>Categorical Visibility Control.</strong>
      <br><br>
      A powerful alternative to the standard FreeCAD Tree View. Instead of hiding objects individually, it toggles visibility based on engineering categories:
      <ul>
        <li><strong>By Layer:</strong> Show/Hide entire production layers (including their associated 3D parts).</li>
        <li><strong>By Robot:</strong> Visualize only the tasks assigned to a specific robot.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/0e065252-4411-4876-ac72-6d780ab41cea" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Load%20WDCurve/upload_icon.svg" width="100px">
    </td>
    <td>
      <h3>Load WDCurve</h3>
      <strong>Native Import & Reconstruction.</strong>
      <br><br>
      Reads external <code>.WDCurve</code> files and fully reconstructs the weld lines within FreeCAD.
      <ul>
        <li><strong>Editable Geometry:</strong> Imported lines are not static; they are converted into native workbench objects with full properties, allowing them to be edited, re-sequenced, or modified as if they were created inside the plugin.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/6d45f013-bd2c-4388-bd8a-4b5ce46a77f6" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Show%20Names/names_icon.svg" width="100px">
    </td>
    <td>
      <h3>Show Names</h3>
      <strong>Orientation & ID HUD.</strong>
      <br><br>
      Toggles a "Head-Up Display" in the 3D view for all weld lines.
      <ul>
        <li><strong>ID Labels:</strong> Shows the name/number of the weld floating above it.</li>
        <li><strong>Direction Markers:</strong> Clearly marks the <strong>Start (O)</strong> and <strong>End (X)</strong> of the path to verify torch direction visually.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/74d28c64-80fd-4a0b-bab3-08fa81ffdf86" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Focus%20on%20Object/focus_icon.svg" width="100px">
    </td>
    <td>
      <h3>Focus on Object</h3>
      <strong>Instant Navigation.</strong>
      <br><br>
      A productivity shortcut that instantly zooms and centers the camera on the object currently selected in the tree or list. Essential for locating small weld segments in large-scale environments.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/86b8d792-165a-4f9a-869f-9d077f8ce722" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Welding%20Reference/reference_icon.svg" width="100px">
    </td>
    <td>
      <h3>Welding Reference Tool</h3>
      <strong>2D Blueprint to 3D Model Synchronization.</strong>
      <br><br>
      The <strong>Welding Reference Tool</strong> allows engineers to work with blueprints, technical images, or diagrams directly within the 3D environment, eliminating the need to keep a PDF open on a second monitor.
      <br><br>
      It enables the import of 2D documentation to place digital markers and logically link them with real 3D objects in the document.
      <br><br>
      <strong>Key Capabilities:</strong>
      <ul>
        <li><strong>Interactive Mapping:</strong> Load any image (PNG, JPG) and place "weld points" simply by clicking on the drawing.</li>
        <li><strong>Digital Linkage:</strong> Associate each 2D mark with an existing weld bead in the 3D model for full traceability.</li>
      </ul>
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_REFERENCE"><img src="https://img.youtube.com/vi/LINK_VIDEO_REFERENCE/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Weld%20Projector/projector_icon.svg" width="100px">
    </td>
    <td>
      <h3>Weld Projector</h3>
      <strong>High-Precision Path Projection.</strong>
      <br><br>
      The <strong>Weld Projector</strong> is designed to process and project welding trajectories with high precision. Its algorithm uses weld faces and physical CAD edges as references to generate accurate weld lines.
      <br><br>
      <strong>Key Capabilities:</strong>
      <ul>
        <li><strong>Precise Mathematical Mapping:</strong> Performs exact mapping of edges onto multiple irregular surfaces, ensuring the weld path adheres perfectly to the part geometry.</li>
        <li><strong>Object Focus:</strong> Automatically focuses on the current selection or processed welds, providing total control over the work environment.</li>
        <li><strong>Start/End Point Validation:</strong> Interactive table integration—clicking on the data table highlights the <strong>Start</strong> and <strong>End</strong> points in the 3D viewer to visually validate the welding direction.</li>
      </ul>
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_PROJECTOR"><img src="https://img.youtube.com/vi/LINK_VIDEO_PROJECTOR/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Weld%20Creator/creator_icon.svg" width="100px">
    </td>
    <td>
      <h3>Weld Creator</h3>
      <strong>Versatile Path Generation & Stitch Patterns.</strong>
      <br><br>
      Designed for versatile and parametric weld path generation. Unlike the Projector, this module focuses on direct creation, allowing for manual path drawing, conversion of existing edges, and the calculation of complex discontinuous (Stitch Weld) patterns.
      <br><br>
      <strong>Key Capabilities:</strong>
      <ul>
        <li><strong>Parametric Stitch Welding:</strong> Advanced algorithm that automatically segments continuous edges into weld patterns, allowing precise control over segment quantity, gap length, and start offsets.</li>
        <li><strong>Freehand Creation:</strong> Manual weld path generation via sequential selection of 3D space points or model vertices.</li>
        <li><strong>Direct Edge Conversion:</strong> Immediate transformation of selected edge chains into weld objects, preserving topology and applying adaptive discretization on curves.</li>
      </ul>
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_CREATOR"><img src="https://img.youtube.com/vi/LINK_VIDEO_CREATOR/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Surface%20Weld/surface_icon.svg" width="100px">
    </td>
    <td>
      <h3>Surface Weld Generator</h3>
      Designed for volumetric modeling and physical representation of joints. Unlike trajectory modules, this tool generates actual solid geometry, allowing the visual representation of Fillet, Butt, and Curve welds for <strong>collision analysis</strong> and technical documentation.
      <br><br>
      <strong>Key Capabilities:</strong>
      <ul>
        <li><strong>Fillet Weld Generation:</strong> Automatic creation of weld prisms between perpendicular faces. The algorithm computes surface normals to correctly orient and extrude the triangular bead along linear joints.</li>
        <li><strong>Curved Surface Adaptation:</strong> Implementation of BSpline interpolation to create smooth, continuous weld beads that organically adapt to curved edges and complex tangencies between faces.</li>
        <li><strong>Guide Constructor:</strong> Integrated utility for drawing manual reference polylines, facilitating the definition of axes and direction vectors in assemblies where automatic geometry requires user assistance.</li>
      </ul>
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_SURFACE"><img src="https://img.youtube.com/vi/LINK_VIDEO_SURFACE/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Weld%20Simulator/simulator_icon.svg" width="100px">
    </td>
    <td>
      <h3>Weld Simulator</h3>
      <strong>Sequence Verification & Cycle Time Analysis.</strong>
      <br><br>
      This module is designed to visualize and verify the entire welding sequence. It simulates continuous torch movement along the generated trajectories, allowing validation of direction, continuity, and cycle times prior to export.
      <br><br>
      <strong>Key Capabilities:</strong>
      <ul>
        <li><strong>Kinematic Validation:</strong> Real-time visualization of the Tool Center Point (TCP) movement over the 3D model. It strictly respects the user-defined travel speed (mm/s) to detect process flow errors and estimate realistic production times.</li>
      </ul>
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_SIMULATOR"><img src="https://img.youtube.com/vi/LINK_VIDEO_SIMULATOR/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Weld%20Visualizer/visualizer_icon.svg" width="100px">
    </td>
    <td>
      <h3>Weld Visualizer (Sphere Mode)</h3>
      <strong>High-Performance Visual Verification.</strong>
      <br><br>
      Designed for rapid visual verification of welds without the computational overhead of generating complex geometric solids.
      <br><br>
      It utilizes direct scene graph rendering (<strong>Coin3D</strong>) to project a "cloud" of spheres along the trajectory, providing an immediate visual representation of weld coverage while maintaining a lightweight model size and fluid viewport navigation.
      <br><br>
      👇 <strong>Feature Demonstration:</strong><br>
      <a href="LINK_VIDEO_VISUALIZER"><img src="https://img.youtube.com/vi/LINK_VIDEO_VISUALIZER/0.jpg" width="200"></a>
    </td>
  </tr>
<tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/RoboDK%20Export/robodk_icon.svg" width="100px">
    </td>
    <td>
</table>

## 🤖 RoboDK & Process Automation

<table>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/RoboDK%20Export%20Tools/export_icon.svg" width="100px">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/RoboDK%20Export%20Tools/export_single.svg" width="100px">
    </td>
    <td>
      <h3>RoboDK Export Tools</h3>
      <strong>Seamless CAD-to-Simulation Transfer.</strong>
      <br><br>
      A dedicated bridge to send geometry directly to RoboDK for simulation. It offers two operation modes for maximum flexibility:
      <ul>
        <li><strong>Export Entire CAD:</strong> Transfers the full visible assembly to the simulation environment in one click.</li>
        <li><strong>Export Selected:</strong> Sends only specific components, perfect for partial updates or isolated testing.</li>
        <li><strong>Auto-Alignment:</strong> Both modes automatically generate and reference the "CAD_Frame" coordinate system, ensuring perfect alignment between the design and the robot station.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
     <video src="https://github.com/user-attachments/assets/5816ddd7-fc37-4e95-8dcf-931552d8a005" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="https://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Glue%20Manager/glue_icon.svg" width="100px">
    </td>
    <td>
      <h3>Glue Manager</h3>
      <strong>Weld-to-Dispensing Path Conversion.</strong>
      <br><br>
      This tool repurposes existing MANUFAI weld paths (`Pts` data) to create precise adhesive dispensing trajectories.
      <ul>
        <li><strong>Non-Destructive Transformation:</strong> Includes a dedicated panel to Scale, Translate, and Rotate the path locally without altering the original CAD geometry.</li>
        <li><strong>Smart Export:</strong> Automatically calculates surface normals for correct gun orientation and exports the transformed data to RoboDK as a "Curve Follow Project".</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/dc94b2dc-10fd-43ca-8ee6-99f1b0e456ef" width="100%" controls></video>
    </td>
  </tr>
  <tr>
    <td width="150" align="center" valign="top">
      <img src="http://raw.githubusercontent.com/jr23mx/MANUFAI_freecad_plugin/refs/heads/main/Drilling%20Manager/Drill.svg" width="100px">
    </td>
    <td>
      <h3>Drilling Manager</h3>
      <strong>Automated Hole & Rivet Processing.</strong>
      <br><br>
      A complete suite for automating drilling or riveting operations. It detects circular edges on the 3D model to extract centers and normal vectors automatically.
      <ul>
        <li><strong>Operation Modes:</strong>
          <ul>
            <li><strong>Manual:</strong> Step-by-step definition (Start/End points) for visual depth control.</li>
            <li><strong>Precision:</strong> Apply specific numeric depth values to single holes.</li>
            <li><strong>Batch Processing:</strong> The "Crown Jewel" feature—select dozens of holes and apply global drilling parameters to all of them instantly.</li>
          </ul>
        </li>
        <li><strong>Full Simulation:</strong> Generates complete Approach, Drill, and Retract targets within RoboDK automatically.</li>
      </ul>
      👇 <strong>Feature Demonstration:</strong><br>
      <video src="https://github.com/user-attachments/assets/f443d37d-f42e-41e8-b491-27f4ca8b8684" width="100%" controls></video>
    </td>
  </tr>
</table>
