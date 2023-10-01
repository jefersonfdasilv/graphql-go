# Go Graphql API
 - This is a simple API using Go and GraphQL
 - This API is based on Go Experts Course
## Command to run
```
go run server.go
```
## Category
### Create a new Category
```
mutation createCategory {
  createCategory(input: {
    name: "Linguagem",
    description: "Linguagens de programação"
  }){
    id,
    name
    description
  }
}
```

### List all Categories
```
query queryCategories {
  categories {
    id
    name,
    description
  }
}
```

### List All Categories With Courses
```
query queryCategoriesWithCourses {
  categories {
    id
    name,
    description,
    courses {
      id
      name
    }
  }
}
```
## Course
### Create a new Course
```
mutation createCourse {
  createCourse(input: {
    name: "Go Lang",
    description: "Curso de Go Lang Avançado"
    categoryId: "df853377-af90-4c2e-9fdc-935242b7c8d2"
  }){
    id,
    name
    description
  }
}
```
### List all Courses
```
query queryCourse {
  courses {
    id
    name
  }
}
```

### List All Courses With Category
```
query queryCourseWithCategories {
  courses {
    id
    name
    description
    category {
      id
      name
    }
  }
}
```
