Below the public DNS ipv4 instances:

mc1 (cloudera manager/ edge-facing client node)	: ec2-18-194-169-169.eu-central-1.compute.amazonaws.com
mc2 (master/worker node)						: ec2-18-194-223-235.eu-central-1.compute.amazonaws.com
mc3 (master/worker node)						: ec2-18-194-112-155.eu-central-1.compute.amazonaws.com
mc4 (worker node)								: ec2-18-194-175-161.eu-central-1.compute.amazonaws.com
mc5 (edge node, only gateway)					: ec2-18-194-177-58.eu-central-1.compute.amazonaws.com

I choose to have only three worker node (DN, NM) leaving free mc1 node for edge-facing client (hue, oozie ...)