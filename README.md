# saucedemo_jmeter

# JMeter Performance Test for Saucedemo

## Overview
This JMeter test script is designed to evaluate the performance of the Saucedemo web application. It simulates multiple virtual users making requests to key application endpoints to assess response times and system behavior under load.

## Test Plan Structure
- **Thread Group:**
  - Number of Threads (Users): `${vusers}` (can be set dynamically)
  - Ramp-up Period: `${rampup}` (can be set dynamically)

- **HTTP Requests:**
  - `GET ${BASE_URL_1}/v1/`
  - `GET ${BASE_URL_1}/v1/inventory.html`
  - `GET ${BASE_URL_1}/v1/index.html`
  
These requests simulate user interactions with the application.

## Setup Instructions
### Prerequisites
1. Install [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi).
2. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/your-repo.git
   ```
3. Open the JMeter script (`saucedemo_jmeter_performance.jmx`) in JMeter.

### Configuring Parameters
Before running the test, configure the required variables:
- **Base URL:** Set `${BASE_URL_1}` to the application endpoint.
- **Virtual Users:** Define `${vusers}` to set the number of concurrent users.
- **Ramp-up Time:** Define `${rampup}` to control the load increase over time.

### Running the Test
1. Open JMeter and load `saucedemo_jmeter_performance.jmx`.
2. Update the test variables in the "User Defined Variables" section.
3. Start the test by clicking the **Run** button.

### Analyzing Results
- Use **View Results Tree** or **Summary Report** listeners to analyze response times.
- Review JMeter logs for any errors.
- Export results for further analysis.

## Contribution
Feel free to submit pull requests or report issues to enhance this performance test.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.