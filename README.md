



# **Log Analysis Script for Cybersecurity Tasks**

## **Overview**
This repository contains a Python-based log analysis script designed to process server logs and extract key insights for cybersecurity-related tasks. The script analyzes log files to detect suspicious activities, identify request patterns, and provide useful metrics for system monitoring and security audits.

---

## **Features**
1. **Count Requests per IP Address**:
   - Extracts and counts the number of requests made by each IP address.
   - Outputs results sorted by request count in descending order.

2. **Identify Most Frequently Accessed Endpoint**:
   - Determines the endpoint (e.g., URL) accessed the most and its frequency.

3. **Detect Suspicious Activity**:
   - Flags IP addresses with failed login attempts exceeding a configurable threshold (default: 10).
   - Detects failed login attempts via specific HTTP status codes (e.g., 401) or error messages.

4. **Export Results**:
   - Saves analysis results to a CSV file (`log_analysis_results.csv`) with:
     - Requests per IP: IP Address, Request Count
     - Most Accessed Endpoint: Endpoint, Access Count
     - Suspicious Activity: IP Address, Failed Login Count

---

## **Usage Instructions**

### **1. Prerequisites**
- Python 3.x
- A log file in plain text format (e.g., Apache or Nginx access logs)

### **2. Running in Google Colab**
1. Open the `Log Analysis Script.ipynb` file in [Google Colab](https://colab.research.google.com).
2. Follow the instructions in the notebook:
   - Upload your log file.
   - Execute the cells sequentially to perform analysis.
3. Download the results as `log_analysis_results.csv` for further use.
   
---

## **File Structure**
- `Log Analysis Script.ipynb`: Google Colab notebook for log analysis.
- `README.md`: Project documentation.
- `sample.log` (optional): Example log file for testing.

---

## **Key Configurations**
- **Log File**: Update the `LOG_FILE` variable in the script or notebook to specify your log file name.
- **Failed Login Threshold**: Adjust the `FAILED_LOGIN_THRESHOLD` to customize detection sensitivity for suspicious activity.

---

## **Sample Output**
### Terminal Output:
```
Requests per IP:
192.168.1.1           234
203.0.113.5           187

Most Frequently Accessed Endpoint:
/home (Accessed 403 times)

Suspicious Activity Detected:
192.168.1.100         56
```

### CSV File:
Saved as `log_analysis_results.csv` with results structured into sections.

---

## **License**
This project is open-source and available under the [MIT License](LICENSE).

---

## **Contributions**
Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

Let me know if you'd like help customizing this README further or if you'd like to include additional sections like testing or examples.
