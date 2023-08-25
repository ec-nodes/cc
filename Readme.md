# Multiple SSH Node Monitoring

 ### 1: Open one of your nodes via SSH and use the following command to create the script:
 <pre> <code id="copy-command"> curl -o ~/status https://raw.githubusercontent.com/ec-nodes/cc/main/status </code> </pre>

 ### 2: Input the data for each node in the format "NodeIP User Pass", saving with CTRL+X, using command:
 <pre> <code id="copy-command"> nano ~/data </code> </pre>
 
  Example data format in the file: <pre> 192.168.170.51 Node1 PassNode1<br>192.168.170.55 Node2 PassNode2 </pre>

 ### 3: Execute the monitoring script using the command:
  <pre> <code id="copy-command"> python3 ~/status </code> </pre>
 
   The script will connect to each node listed in the "data" file, retrieve status information, and display the results.

# Output

The script will display a table with the following information for each monitored node:

- Node IP: The IP address of the node.
- Last Call: The time elapsed since the last contract call.
- Status: The node's status, including "Active" or "Failed".

Example output:
<br><br>Node IP -------------- Last Call ---------- Status
<br>----------------------------------------------------------------
<br>192.168.170.51: 03h, 43min ago - Active
<br>191.168.170.55: 39h, 10min ago - Failed


## Usage Note

This script is intended for use within your own network, regardless of the operational status of the Bloxberg website.

## License

This script is open-source and distributed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Disclaimer

Please note that this script is provided "as-is" and without warranty. Use it responsibly and ensure that you have proper authorization to access and monitor the remote nodes.

---

Feel free to contribute to this repository by reporting issues or submitting pull requests to ec.node.monitor@gmail.com
