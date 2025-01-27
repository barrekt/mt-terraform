# mt-terraform
Repository for Terraform-101 Udemy course with Mark Tinderholdt.

Repo contains written notes (kept in this readme.md), and various snippets of terraform code.


# Key Terminology

<b>Idempotency</b><br> An operation that can be applied multiple times without changing the result beyond the initial application. If you perform the operation once or multiple times, the outcome will always be the same.


In the context of Terraform, idempotency ensures that applyign the same configuration multiple times will always produce the same result. If you run **terraform apply** once or multiple times, the state of your infrastructure will remain consistent and unchanged after the first successful application. 

Example - if you define a resource in Terraform and apply the configuration, Terraform will create that resource. If you apply the same connfig again, Terraform will recognise that the resource already exists & will not attempt to create it again, ensuring no unintended changes or duplications occur.


<b>Immutability</b><br> The concept that once an object is created, it cannot be changed or modified in-place. Instead, any changes result in the creation of a new object. 


Immutability is a principle that aligns with the c oncept of infrastructure as code. When you apply changes to your TF config, Terraform will create new resources if necessary and destroy the old ones, rather than modifying existing resources. Immutability is often the North Star of Infrastructure deployments - counteracting the 'ClickOps' approach.

Managing mutable control planes such as manually changing an OS config, cloud control plane, by creating artifacts with a desired state of a configuration so that we can deployments back to a known state. By combining version control (Git) with infrastructure as code (Terraform), we have a full history of artifacts of desired states.

<b>Encapsulation</b></br> Fundamental concept of object-orientated programming, refers to the bundling of data & methods that operate on that data within a single unit, typically a class. Direct access to some of an object's components are restricted, which can help prevent unintended interference.

Terraform works by encapsulating functionality inside of your terraform modules. 




