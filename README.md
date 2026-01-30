<h1 align="center">🌿 YOLO Agricultural Disease Detection</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Model-YOLO-green?style=for-the-badge" alt="YOLO">
  <img src="https://img.shields.io/badge/Framework-PyTorch-red?style=for-the-badge" alt="PyTorch">
  <img src="https://img.shields.io/badge/Field-AgriTech-blue?style=for-the-badge" alt="AgriTech">
</p>

<hr>

<h2>🖼️ Visual Results & Performance</h2>

<p align="center">
  <table width="100%">
    <tr>
      <td align="center"><b>Original Raw Image</b></td>
      <td align="center"><b>Model Prediction (Inference)</b></td>
    </tr>
    <tr>
      <td><img src="Data/sample_raw.jpg" alt="Raw Data" width="100%"></td>
      <td><img src="Test_predictions/sample_pred.jpg" alt="Prediction" width="100%"></td>
    </tr>
  </table>
</p>

<h3>📈 Performance Metrics</h3>
<p align="center">
  <img src="metric_charts/results.png" alt="Training Metrics" width="90%">
</p>



<hr>

<h2>📂 Detailed Directory Breakdown</h2>

<table width="100%">
  <tr>
    <th width="25%">Directory</th>
    <th width="75%">Technical Description</th>
  </tr>
  <tr>
    <td><b>📁 Data</b></td>
    <td><b>Source Dataset:</b> Contains the original, unedited imagery categorized into <code>fito</code>, <code>monilia</code>, and <code>sana</code> (healthy). This serves as the ground-truth reference before any preprocessing or augmentation.</td>
  </tr>
  <tr>
    <td><b>📁 Images</b></td>
    <td><b>Processed Visuals:</b> Images here are resized and formatted for the YOLO architecture. Divided into <code>/train</code> and <code>/val</code> folders to prevent data leakage during the learning phase.</td>
  </tr>
  <tr>
    <td><b>📁 Labels</b></td>
    <td><b>Annotation Files:</b> Contains <code>.txt</code> files for every image in the <i>Images</i> folder. Each file follows the YOLO format: <code><class_id> <x_center> <y_center> <width> <height></code>.</td>
  </tr>
  <tr>
    <td><b>📁 metric_charts</b></td>
    <td><b>Analytics Hub:</b> Houses generated plots including the Confusion Matrix (to see misclassifications between Fito and Monilia), F1-Score curves, and Precision-Recall charts.</td>
  </tr>
  <tr>
    <td><b>📁 Models</b></td>
    <td><b>Weights Library:</b> 
      <ul>
        <li><code>best.pt</code>: The weights that achieved the highest mAP (mean Average Precision).</li>
        <li><code>last.pt</code>: The state of the model at the final epoch.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><b>📁 runs</b></td>
    <td><b>Training Logs:</b> The raw output of the Ultralytics training engine. Includes per-epoch loss values (box_loss, cls_loss, dfl_loss) and hyperparameters used.</td>
  </tr>
  <tr>
    <td><b>📁 Test</b></td>
    <td><b>Hold-out Dataset:</b> A curated set of images that the model never saw during training or validation, used to calculate the real-world generalization error.</td>
  </tr>
  <tr>
    <td><b>📁 Test_predictions</b></td>
    <td><b>Inference Output:</b> The final visual proof of the model's capability. Images here show bounding boxes with confidence scores for the three target classes.</td>
  </tr>
</table>

<hr>

<h2>📝 Core Implementation</h2>

<p>The entire logic for this project is contained within:</p>
<ul>
  <li><b><code>YOLO_Deep_Learning.ipynb</code></b>: A comprehensive Jupyter Notebook that covers environment setup, data YAML configuration, model instantiation, training, and automated plotting of results.</li>
</ul>

<hr>

<h2>🚀 How to Use</h2>

<ol>
  <li>Clone this repository.</li>
  <li>Install dependencies: <code>pip install ultralytics</code></li>
  <li>Open <code>YOLO_Deep_Learning.ipynb</code> and run the cells to perform inference using <code>Models/best.pt</code>.</li>
</ol>

<p align="center">
  <b>Developed for Precision Agriculture & Disease Management</b>
</p>