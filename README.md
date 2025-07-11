### Inter Mixer Performance Analysis in 3D Printing

<p align="justify">This code is designed to evaluate the performance of an inter-mixer using advanced image processing techniques. The overall workflow is divided into two main stages: image preparation and image analysis, each serving a critical role in assessing the quality of material mixing.</p>
<b>1. Image Preparation </b>
<p align="justify">The first step involves preprocessing the image to ensure accurate analysis. During image acquisition, an unavoidable yellow lighting artifact was introduced, which altered the true appearance of the specimen's color. To correct this, the code applies image enhancement techniques to remove the yellow light, thereby restoring the specimen’s original color profile and ensuring reliable results in the subsequent analysis.</p>
<b>2. Image Analysis</b>
<p align="justify">Once the image has been corrected, it undergoes a comprehensive analysis to evaluate the inter-mixer's effectiveness in blending two colors (typically red and blue). This analysis is performed using three complementary methods:</p>
<i>•	Histogram Analysis:</i>  <p align="justify"> Examines the distribution of color intensities across the image and compares the red and blue channels using metrics such as entropy, correlation, and histogram intersection to evaluate the uniformity and quality of the mix.</p>
<i>•	Standard Index Analysis:</i> <p align="justify"> Applies well-established statistical indices, including Structural Similarity Index (SSIM), Mean Squared Error (MSE), Mutual Information, Normalized Cross-Correlation (NCC), and KL-Divergence to quantitatively assess how well the two colors are integrated.</p>
<i>•	Cluster Analysis:</i> <p align="justify">Uses clustering algorithms (e.g., k-means) to group similar color regions within the image. It determines the optimal number of clusters using methods like the Elbow Method and Davies-Bouldin Index, and visualizes the color distribution within each cluster, providing a detailed view of how uniformly the colors are blended.</p>
After clustering, the color composition within each cluster is analyzed. This includes calculating the average intensity of red and blue in each group, which helps to understand how dominant or balanced the colors are in different regions of the image.<br/><br/>
<p align="justify"> By integrating these methods, the code provides a robust, multi-faceted assessment of mixing performance. It allows for clear comparison across different inter-mixer configurations and effectively identifies the best-performing inter-mixer based on objective, quantifiable image characteristics.</p>
<br/><br/>
<img src="Code_Flow_Chart.png">
