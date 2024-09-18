# Node-RED Flow for Fetching Quotes
This Node-RED flow fetches quotes from the API Ninjas service and displays them in the debug panel.
### 1. Inject Node
- **Purpose**: This node is used to manually trigger the flow or set it to trigger at specific intervals.
- **Configuration**:
  - **Payload**: Set to `timestamp` (default).
  - **Repeat**: Leave it empty for manual trigger or set a time interval.
  - **Wires**: Connects to the HTTP Request node.

### 2. HTTP Request Node
- **Purpose**: This node makes an HTTP GET request to fetch quotes from the API Ninjas service.
- **Configuration**:
  - **Method**: Set to `GET`.
  - **URL**: `https://api.api-ninjas.com/v1/quotes?category=happiness&X-Api-Key=Your_API_Key_Here`
  - **Return**: Set to `a parsed JSON object`.
  - **Wires**: Connects to the Debug node.

### 3. Debug Node
- **Purpose**: This node displays the output of the HTTP request in the debug panel.
- **Configuration**:
  - **Output**: Set to `msg.payload` to display the response from the API.
  - **Wires**: No further connections.

### Step-by-Step Setup

1. **Install Node-RED**:
    ```bash
    npm install -g --unsafe-perm node-red
    ```

2. **Start Node-RED**:
    ```bash
    node-red
    ```

3. **Access Node-RED**:
    Open your browser and navigate to `http://localhost:1880`.

4. **Import the Flow**:
    - Copy the JSON code provided.
    - In Node-RED, click on the menu (top right corner) -> Import -> Clipboard.
    - Paste the JSON code and click on "Import".

5. **Configure the HTTP Request Node**:
    - Double-click the HTTP request node.
    - Replace `Your_API_Key_Here` with your actual API key from API Ninjas.

6. **Deploy the Flow**:
    - Click the "Deploy" button on the top right to save and run your flow.

### Contact

For any queries or support, feel free to reach out:

- **Email**: [keerthi.ece.software@gmail.com](mailto:keerthi.ece.software@gmail.com)
  
## License
- This project is licensed under the MIT License
