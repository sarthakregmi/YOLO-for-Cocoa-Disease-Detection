<h1 align="center">YOLO Disease Detection: Fito, Monilia, and Sana</h1>

<p align="center">
  <em>An end-to-end deep learning pipeline for agricultural disease classification and localization using YOLO.</em>
</p>

<hr>

<h2>📂 Project Structure</h2>

<table width="100%">
  <thead>
    <tr>
      <th align="left">Folder/File</th>
      <th align="left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>📁 Data</b></td>
      <td>Raw dataset classified into categories: <i>Fito, Monilia, and Sana</i>.</td>
    </tr>
    <tr>
      <td><b>📁 Images</b></td>
      <td>Training and Validation image sets derived from raw data.</td>
    </tr>
    <tr>
      <td><b>📁 Labels</b></td>
      <td>Bounding box annotations in <code>.txt</code> format.</td>
    </tr>
    <tr>
      <td><b>📁 metric_charts</b></td>
      <td>Accuracy, Loss, and mAP assessment visualizations.</td>
    </tr>
    <tr>
      <td><b>📁 Models</b></td>
      <td>Stored <code>best.pt</code> and <code>last.pt</code> weights from training.</td>
    </tr>
    <tr>
      <td><b>📁 runs</b></td>
      <td>Detailed logs and data captured during each training epoch.</td>
    </tr>
    <tr>
      <td><b>📁 Test</b></td>
      <td>Unseen dataset for final model evaluation.</td>
    </tr>
    <tr>
      <td><b>📁 Test_predictions</b></td>
      <td>Output images featuring predicted bounding boxes.</td>
    </tr>
    <tr>
      <td><b>📄 YOLO_Deep_Learning.ipynb</b></td>
      <td>Main Jupyter Notebook containing the full training pipeline.</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>🚀 Workflow</h2>

<p>The project follows a standard Computer Vision pipeline:</p>
<ol>
  <li><b>Preprocessing:</b> Raw data is cleaned and split into 80/20 training and validation sets.</li>
  <li><b>Training:</b> The YOLO model is trained via the <code>YOLO_Deep_Learning.ipynb</code> notebook.</li>
  <li><b>Evaluation:</b> Performance is monitored via <code>metric_charts</code> to ensure no overfitting.</li>
  <li><b>Inference:</b> The final model is deployed on the <code>Test</code> set to generate <code>Test_predictions</code>.</li>
</ol>



<hr>

<h2>🛠️ Environment Setup</h2>

<p>To replicate this project, ensure you have the following installed:</p>

<code>pip install ultralytics opencv-python matplotlib</code>

<hr>

<p align="center">
  <i>Developed for Automated Agricultural Inspection</i>
</p>