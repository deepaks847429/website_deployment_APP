<h1>Upload service</h1>
->Install Node.js
->Initialise an empty typescript project
->Basic typescript configuration
->Add express , redis , aws-sdk , simple-git , cors as dependencies
->Initialize a simple express app in index.ts    listening on port 3000
->Initialise an endpoint that the user will hit and send the repo url as input
->Create a function that randomly generates an id for this session. Call it generate
->Use simple-git to clone the repo into a new folder (/out/id ).
->Write a function that gets the paths of all  the files in the /out/id folder
->Create an AWS account
->Write a function that uploads a file given a path to S3
->Iterate over all the files and upload them to S3 one by one (or together)
->Start redis locally
->Initialize a redis publisher
->Use redis queues to push the uploadId in the queue
->Also store the current video id’s status as uploaded .
->Expose a status endpoint that the frontend will poll to get back the     status of a video. It needs to check redis for the current value.


<h1>Deploy service</h1>
->Initialise an empty typescript project.
->Configure the tsconfig.json.
->Create an infinitely running for loop that pulls values from the redis queue.
->Write a function called downloadS3Folder that downloads all the files from a given location in S3.
->Run npm run build to convert the React code into HTML/CSS files. (Bonus if this is containerized).
->Write a function that uploads a directory to S3 (you can copy it from the last module).
->Store in the redis database that this specific upload has been processed.


<h1>Request handler</h1>
 
->Initialize a Node.js Project, add TS configurations
->Initialize an express server running on port 3001
->Add a global route catch (/*) which handles all requests
->Extract the sub-domain the request is coming from (id.vercel.com ⇒ id)
->Get the contents from S3 assuming the subdomain represents the id and forward it to the user. Add the correct content-type header to ensure the final file is parsed as a html file.

<h1>Frontend</h1>

->The project involves building a simple form that let’s users send requests to the services we made in the last points