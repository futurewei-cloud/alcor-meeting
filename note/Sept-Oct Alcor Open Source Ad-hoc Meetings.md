# Alcor Open Source Community Meeting 09/30, 10/3, 10/7, 10/10， 10/14


    MIT License
    Copyright(c) 2020 Futurewei Cloud

    Permission is hereby granted,
    free of charge, to any person obtaining a copy of this software and associated documentation files(the "Software"), to deal in the Software without restriction,
    including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and / or sell copies of the Software, and to permit persons
    to whom the Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
    WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

##  Network Intelligence Collaboration Meeting Notes

### 9/30/2022
Discussed the required contents of the final report

### 10/3/2022
Based on the final report template, we went through the details of each section. Designed the experiment plan of models.

### 10/7/2022
Checked the contents of final report draft and refined the model architecture and model training parameters.

### 10/10/2022
Discussed the current experiment results and model improvement. Also discussed about some potential future work of this project.

### 10/14/2022
Went through the final report details and identified the revision items, including the mathematical formula of attention network design, input embedding, clustering modeling, and configuration aggregation.

Discussed the results under various thresholds after lowering the learning rate and increasing the training epochs. Found the optimal threshold of the current testing dataset.

Discussed the appropriate way to present the results, including bar charts, line charts, and tables. The results will be presented based on the contents of the working scenario, where the true positive means prediction hit, the false negative means the prediction miss (will trigger on-demand request later), and the false positive means the redundant deployment.