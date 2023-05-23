To test the script as a kubectl plugin, follow these steps:

Save the modified script to a file, e.g., kubeplugin.

Make the script executable: chmod +x kubeplugin.

Move the script to a location in your $PATH (e.g., /usr/local/bin) or add the directory containing the script to your $PATH.

Run the script as a kubectl plugin:

$ kubectl plugin-name <namespace> <command> <resource_type>

Replace <namespace>, <command>, and <resource_type> with the appropriate values.

For example, to retrieve statistics from the kube-system namespace for pods:

$ kubectl kubeplugin kube-system get pods
  
The script will output the statistics in the format: "Resource, Namespace, Name, CPU, Memory" for each resource.

Once you have tested the script and confirmed it's working correctly, you can commit it to the scripts directory of your repository.

Note: Ensure that you have the necessary permissions and access to the Kubernetes cluster before running the script.
