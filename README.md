<h1>Network Pruning of CNN</h1>
<h6>3rd Project - NCAI, DLL internship</h6>

<h4>Project description:</h4>
<p>Network Pruning is a concept of reducing the size of a model by removing weights which do not have a significant contribution during inference, with the objective of getting a lighter and faster version of a model that could be deployed on hardware limited resources e.g. IoT devices. In my implementation of network pruning, redundant weights are removed after training has been completed.</p>


<h3>Project Workflow:</h3>
<ol>
  <li>Data Loading</li>
  <li>Model design</li>
  <li>Model Training</li>
  <li>Filters Identification</li>
  <li>Pruning</li>
  <li>Pruned Model's reconstruction</li>
  <li>Fine Tuning</li>
</ol>

<p>A convolutional neural network with 4 conv blocks is designed and trained on cats_vs_dogs dataset for binary classification. After training, each filter is removed one at a time and after each removal the test data is evaluated by the model to determine the accuracy change. If the accuracy has not changed by a significant value, the filter is marked as redundant. At the end 3 types of filters are identified, 1. Filters when removed, the accuracy decreases, 2. Filters when removed, the accuracy increases and 3. Filters when removed, no significant change in accuracy.</p>

<h3>Results</h3>
<p>The best results i got are as follows:</p>
<table>
  <tr>
    <th>Metrics</th>
    <th>Before Pruning</th>
    <th>After Pruning</th>
  </tr>
  <tr>
    <td>No. of Paras</td>
    <td>262,370</td>
    <td>11,705</td>
  </tr>
  <tr>
    <td>Test Accuracy</td>
    <td>0.8850</td>
    <td>0.8200</td>
  </tr>
  <tr>
    <td>Test Loss</td>
    <td>0.3480</td>
    <td>0.4539</td>
  </tr>
  <tr>
    <td>Time per Step</td>
    <td>43ms/step</td>
    <td>14ms/step</td>
  </tr>
</table>

<p>Accuracy Drop: <b>7.24%</b></p>
<p>Size Reduction: <b>95.53%</b></p>
