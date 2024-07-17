# WORDPRESS

To run the wordpress follow below steps :-

1.  firstly clone the repository.

       `git clone <repository-link>`

2. To deploy the wordpress run following commands.

    `kubectl apply -f WORDPRESS-WITH-KUBERNETES`

3. then run this command to forward the port to localhost.

   `kubectl port-forward svc/wordpress 3838:3838`