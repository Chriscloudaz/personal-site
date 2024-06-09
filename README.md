# Chris Parbey - Personal Site

## Project Architecture
The site is built using microservices architecture and is hosted on a Kubernetes cluster. It comprises of four separate applications (main site, blog, cloud resume, and games) all deployed in different namespaces on the cluster.

The blog's frontend is connected to a managed RDS (Relational Database Service) instance, ensuring reliable and scalable database management.

DNS in managed with AWS Route53.

Continuous deployment is automated with GitHub Actions, streamlining updates and ensuring seamless integration of new features.

## Links
- **Main site**: [parbtechsolutions.com](https://parbtechsolutions.com/)
- **Blog**: [blog.parbtechsolutions.com](https://blog.parbtechsolutions.com/)
- **Cloud resume**: [resume.parbtechsolutions.com](https://resume.parbtechsolutions.com/)
- **Games**: [games.parbtechsolutions.com](https://games.parbtechsolutions.com/)
  
## Repo Structure

 - `.github/workflows/`: Directory contains Github Actions CI/CD
   configurations for all four applications.
  - `blog`: Directory contains the blog deployment manifest. 
  - `games`: Directory contains the game deployment manifest.
  - `main-site`: Contains the main website files (index.html, css, Dockerfile, and deployment manifest)
  - `resume-site`: Contains the cloud resume files (index.html, css
   files, Dockerfile, and deployment manifest)

  

# Cloud Services Used
 - AWS Route53 
 - Digital Ocean Kubernetes Cluster 
 - Digital Ocean Container Registry 
 - Digital Ocean Managed RDS 
 - Github Actions