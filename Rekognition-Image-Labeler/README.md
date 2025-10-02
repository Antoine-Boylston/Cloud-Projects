## Project Overview ☁️

This project walks through building an **Image Label Generator** using **Amazon Rekognition**. Given an image (stored in **Amazon S3**), Rekognition is called to detect objects then returns labels with confidence scores. For example, a casual lunch photo can yield labels like *tableware*, *bottle*, or *person* with their confidences.

---

## Roadmap

We’ll go through the following steps:

1. Create an **Amazon S3** bucket  
2. Upload sample images to S3  
3. Install and **configure the AWS CLI**  
4. Set up a **Python virtual environment** and install dependencies (`boto3`)  
5. Implement a `detect_labels` function  
6. Add a `main` entry point to call it  
7. Run the Python script and review the output
8. (Optional) Teardown to clean up resources.


---

## Final Result

<!-- Replace with screenshots, sample output, or a short clip -->
- **Expected output:** a list of labels with confidence scores for each image
- **Example:** `Label: "Bottle" (98.7%), "Tableware" (95.2%)`

---

## Services Used 🛠

| Service            | Purpose                                           | Notes                                  |
|--------------------|---------------------------------------------------|----------------------------------------|
| **Amazon S3**      | Store input images                                | Keep bucket and Rekognition **regions aligned** |
| **Amazon Rekognition** | Analyze images and return labels                | Pay-per-use; Free Tier eligibility may apply |
| **AWS CLI**        | Interact with AWS from the terminal               | Verify credentials/region; manage S3   |

---

## Estimated Time & Cost

> ⚠️ Approximations only. 

**Build Time (one-time):**
| Phase              | Estimate      |
|--------------------|---------------|
| Planning           | ~10 min       |
| Provision infra    | ~10 min       |
| App/deploy & tests | ~20 min       |

**Monthly Cost (steady state):**
| Component            | Qty | $/Month (est.) | Notes                                   |
|---------------------|-----|----------------|-----------------------------------------|
| S3 bucket           | 1   | ~$0–$1         | Depends on storage/requests             |
| Amazon Rekognition  | —   | ~$0–$1         | Depends on number of images analyzed    |
| AWS CLI             | —   | $0             | CLI tool itself is free                 |
| **Total (est.)**    |     | **~$0–$2**     | Small tests typically cost pennies      |

---

## Architecture Diagram

![Architecture Diagram](architecture/diagram.png)
<small>
**Flow:** Developer machine → AWS CLI/Python → S3 (images) → Rekognition (label detection) → Console/Logs (results).  
**Notes:** Ensure your **AWS region** and **credentials/SSO session** are valid before running.
</small>

---

## Prerequisites

- AWS account with permissions for S3 and Rekognition  
- **AWS CLI v2** installed and configured (`aws --version`, `aws sso login` or access keys)  
- **Python 3.x** and `boto3` (recommend a virtual environment)

---

# Let’s Build!

## Create an Amazon S3 Bucket
<!-- Add your bucket name, region, and creation steps here -->




