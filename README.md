# testGraphQLProject
To know basic of graphql

## in graphql 
### To query in graphql define following 
 1) scheam --> 2) query ----> 3) resolver 
### To Create Resource and Change them we need to define mutation
 1) scheam --> 2) mutation ---> 3) resolver 

### Query Example with variable 

### Write your query or mutation here

 query JobQuery($id:ID!){
  job(id:$id){
    id
    title
    company{
       id
      name
      
    }
    description
    
  }
}

### Variable 

{
  "id": "rJKAbDd_z"
}

------------
query CompanyQuery($id: ID!){
  company(id:$id){
    id
    name
    description
    jobs {
      id
      title
      description
    }
  }
}

variable:
{
  "id": "HJRa-DOuG"
}

----------------------------

## Mutation example 

mutation{
  createJob(title:"Tester",
            description:"With the testing ability", 
             companyId:"SJV0-wdOM")
}

* When mutation is returning a type (in the following example mutation returns type Job)

mutation{
  createJob(title:"Tester",
            description:"With the testing ability", 
             companyId:"SJV0-wdOM"){
     id
    title
    company {
      name
    }
  }
}