# 🎨 ColorFlow

*Retrieval-Augmented Image Sequence Colorization*

**Authors:** Junhao Zhuang, Xuan Ju, Zhaoyang Zhang, Yong Liu, Shiyi Zhang, Chun Yuan, Ying Shan

<a href='https://zhuang2002.github.io/ColorFlow/'><img src='https://img.shields.io/badge/Project-Page-Green'></a> &nbsp;
<a href='https://huggingface.co/spaces/TencentARC/ColorFlow'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Demo-blue'></a> &nbsp;
<a href="https://arxiv.org/abs/2412.11815"><img src="https://img.shields.io/badge/arXiv-2412.11815-b31b1b.svg"></a> &nbsp;
<a href="https://huggingface.co/TencentARC/ColorFlow"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Model-blue"></a>

**Your star means a lot for us to develop this project!** :star:

<img src='https://zhuang2002.github.io/ColorFlow/fig/teaser.png'/>

### 🌟 Abstract 

Automatic black-and-white image sequence colorization while preserving character and object identity (ID) is a complex task with significant market demand, such as in cartoon or comic series colorization. Despite advancements in visual colorization using large-scale generative models like diffusion models, challenges with controllability and identity consistency persist, making current solutions unsuitable for industrial application.

To address this, we propose **ColorFlow**, a three-stage diffusion-based framework tailored for image sequence colorization in industrial applications. Unlike existing methods that require per-ID finetuning or explicit ID embedding extraction, we propose a novel robust and generalizable **Retrieval Augmented Colorization** pipeline for colorizing images with relevant color references.

Our pipeline also features a dual-branch design: one branch for color identity extraction and the other for colorization, leveraging the strengths of diffusion models. We utilize the self-attention mechanism in diffusion models for strong in-context learning and color identity matching.

To evaluate our model, we introduce **ColorFlow-Bench**, a comprehensive benchmark for reference-based colorization. Results show that ColorFlow outperforms existing models across multiple metrics, setting a new standard in sequential image colorization and potentially benefiting the art industry.

### 📰 News

- **Update Date:** December 23, 2024 - We have released the weights for the Sketch_Shading model, along with updates to the related code and demo. You can access the model weights in our [Hugging Face model repository](https://huggingface.co/TencentARC/ColorFlow) and explore the updated demo [here](https://huggingface.co/spaces/TencentARC/ColorFlow). 🎉🔥

- **Release Date:** December 17, 2024 - The inference code and model weights have also been released! 🎉

### 📋 TODO

- ✅ Release inference code and model weights
- ⬜️ Release training code

### 🚀 Getting Started

Follow these steps to set up and run ColorFlow on your local machine:

- **Clone the Repository**
  
  Download the code from our GitHub repository:
  ```bash
  git clone https://github.com/TencentARC/ColorFlow
  cd ColorFlow
  ```

- **Set Up the Python Environment**

  Ensure you have Anaconda or Miniconda installed, then create and activate a Python environment and install required dependencies:
  ```bash
  conda create -n colorflow python=3.8.5
  conda activate colorflow
  pip install -r requirements.txt
  ```

- **Run the Application**

  You can launch the Gradio interface for ColorFlow by running the following command:
  ```bash
  python app.py
  ```

- **Access ColorFlow in Your Browser**

  Open your browser and go to `http://localhost:7860`. If you're running the app on a remote server, replace `localhost` with your server's IP address or domain name. To use a custom port, update the `server_port` parameter in the `demo.launch()` function of app.py.

### 🎉 Demo

You can [try the demo](https://huggingface.co/spaces/TencentARC/ColorFlow) of ColorFlow on Hugging Face Space.

### 🛠️ Method

The overview of ColorFlow. This figure presents the three primary components of our framework: the **Retrieval-Augmented Pipeline (RAP)**, the **In-context Colorization Pipeline (ICP)**, and the **Guided Super-Resolution Pipeline (GSRP)**. Each component is essential for maintaining the color identity of instances across black-and-white image sequences while ensuring high-quality colorization.

<img src="https://zhuang2002.github.io/ColorFlow/fig/flowchart.png" width="1000">

🤗 We welcome your feedback, questions, or collaboration opportunities. Thank you for trying ColorFlow!

### 📄 Acknowledgments

We would like to acknowledge the following open-source projects that have inspired and contributed to the development of ColorFlow:

- **ScreenStyle**: https://github.com/msxie92/ScreenStyle
- **MangaLineExtraction_PyTorch**: https://github.com/ljsabc/MangaLineExtraction_PyTorch

We are grateful for the valuable resources and insights provided by these projects.

### 📞 Contact

- **Junhao Zhuang**  
  Email: [zhuangjh23@tsinghua.org.cn](mailto:zhuangjh23@tsinghua.org.cn)

### 📜 Citation

```
@article{zhuang2024colorflow,
  title={ColorFlow: Retrieval-Augmented Image Sequence Colorization},
  author={Zhuang, Junhao and Ju, Xuan and Zhang, Zhaoyang and Liu, Yong and Zhang, Shiyi and Yuan, Chun and Shan, Ying},
  journal={arXiv preprint arXiv:2412.11815},
  year={2024}
}
```

### 📄 License

Please refer to our [license file](LICENSE) for more details.
