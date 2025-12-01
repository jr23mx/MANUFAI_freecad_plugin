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
      <a href="LINK_VIDEO_ORIGEN"><img src="https://img.youtube.com/vi/LINK_VIDEO_ORIGEN/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_CENTRO"><img src="https://img.youtube.com/vi/LINK_VIDEO_CENTRO/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_ALINEACION"><img src="https://img.youtube.com/vi/LINK_VIDEO_ALINEACION/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_MOVER"><img src="https://img.youtube.com/vi/LINK_VIDEO_MOVER/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_DATA"><img src="https://img.youtube.com/vi/LINK_VIDEO_DATA/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_LINEWELD"><img src="https://img.youtube.com/vi/LINK_VIDEO_LINEWELD/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_TABLE"><img src="https://img.youtube.com/vi/LINK_VIDEO_TABLE/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_SELECTION"><img src="https://img.youtube.com/vi/LINK_VIDEO_SELECTION/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_ASSIGN"><img src="https://img.youtube.com/vi/LINK_VIDEO_ASSIGN/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_VISIBILITY"><img src="https://img.youtube.com/vi/LINK_VIDEO_VISIBILITY/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_WDCURVE"><img src="https://img.youtube.com/vi/LINK_VIDEO_WDCURVE/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_NAMES"><img src="https://img.youtube.com/vi/LINK_VIDEO_NAMES/0.jpg" width="200"></a>
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
      <a href="LINK_VIDEO_FOCUS"><img src="https://img.youtube.com/vi/LINK_VIDEO_FOCUS/0.jpg" width="200"></a>
    </td>
  </tr>
</table>
