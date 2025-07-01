# Brain Tumor MRI Analysis System

This is a complete end-to-end system for brain tumor MRI image analysis. It includes multiple stages—beginning with image filtration and ending with LLM-powered medical report generation—along with a web interface for doctors and medical staff.

## Repository Structure

| Stage | Repository | Description |
|-------|------------|-------------|
| Frontend | [MRI-System](https://github.com/deiaamohamed/MRI-System) | Web interface with separate dashboards for doctors and receptionists, designed for managing patients and uploading MRI scans. |
| Stage 1 | [brain-MRI-filtration](https://github.com/deiaamohamed/brain-MRI-filtration) | Pre-processing and filtering of raw MRI images to enhance quality and remove noise. |
| Stage 2 | [Mask_RCNN_MRI](https://github.com/Omar-Ezzat-AbdAlmoaz/Mask_RCNN_MRI) | Tumor segmentation using a customized Mask R-CNN model trained on brain MRI datasets. |
| Stage 3 | [LLM-REPORTING](https://github.com/deiaamohamed/LLM-REPORTING) | Medical captioning and report generation using BioMedCLIP and other vision-language models. |
| Final Stage | [Brain-Scan-Hub](https://github.com/deiaamohamed/Brain-Scan-Hub) | Integrates all stages into one deployable system with a doctor-friendly interface. |

## Full Pipeline Overview

1. **Image Upload**  
   MRI images are uploaded through the [MRI-System](https://github.com/deiaamohamed/MRI-System) web interface.

2. **Image Pre-processing**  
   In [brain-MRI-filtration](https://github.com/deiaamohamed/brain-MRI-filtration), the uploaded images are denoised, normalized, and resized to a standard format for model compatibility.

3. **Tumor Segmentation**  
   The pre-processed images are passed to the [Mask_RCNN_MRI](https://github.com/Omar-Ezzat-AbdAlmoaz/Mask_RCNN_MRI) module which performs instance segmentation of the tumor area.

4. **LLM-Powered Captioning and Reporting**  
   The segmented output is sent to the [LLM-REPORTING](https://github.com/deiaamohamed/LLM-REPORTING) module which:
   - Crops the tumor area.
   - Enhances visual inputs with overlays.
   - Generates medical captions using BioMedCLIP.
   - Converts captions into full diagnostic reports using an LLM.

5. **Deployment and Integration**  
   The final system is packaged in [Brain-Scan-Hub](https://github.com/deiaamohamed/Brain-Scan-Hub), providing:
   - Patient management.
   - Role-based dashboards (doctor/receptionist).
   - End-to-end flow from image upload to report generation.

## Features

- Role-based authentication (Doctor, Receptionist)
- MRI image upload and processing
- Tumor segmentation with overlays
- Auto-generated diagnostic reports using AI
- Clean web UI with dark mode and animations
- Designed with medical professionals in mind

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend and Models**: Python, Django, Jupyter Notebooks
- **Machine/Deep Learning**: Mask R-CNN, BioMedCLIP, LLMs
- **Libraries**: PyTorch, OpenCV, NumPy, Pandas, Transformers, Matplotlib
- **Deployment**: Local and cloud-ready integration

## Contributors

- Deiaa Mohamed  
- Omar Ezzat  
- Alaa Mohamed  
- Mariam Ayman  
- Mariam Adel  
- Raghad Bayoume  

## Future Work

- Add tumor classification (benign vs malignant)
- Expand database with real hospital data (with consent)
- Add support for DICOM image formats

## Demo and Screenshots

Coming soon – You can clone each repository and run the modules as outlined in their individual README files.

## License

This project is for educational and research purposes only. Clinical use requires validation by certified medical professionals.

## Contact

For collaboration, questions, or improvements:  
**deiaa100g@gmail.com**
