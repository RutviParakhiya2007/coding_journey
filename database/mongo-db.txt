                                                    Mongo DB (NoSql-database)

#_What is mongo-db?
MongoDB is an open-source, document-oriented NoSQL database. (BSON = binary format of JSON)

#_JSON vs BSON :- 
-JSON is human-readable and used for data exchange.
-BSON is optimized for internal database operations.

#_SQL Database (Relational DB) :-
It uses tables(rows & columns) and it is best for structured data.
    e.g. - MySQL, PostgreSQL

#_NoSQL Database :-
It uses documents, key-value, graphs and it is best for flexible/unstrucutred data.
    e.g. - MongoDB, Firebase

#_MongoDB commonly use in : 
    - Web applications
    - Backend Services
    - Real-time Services
    - Data analytics platforms

#_MongoDB vs Relational Database :-

       aspect   |Relational Database|               MongoDB
    ------------+-------------------+--------------------------------
     data model |tables(rowscolumns)|             Documents
       Schema   |      Fixed        |             flexible
       Scaling  |     vertical      |            Horizontal
    Relationship|       joins       |Embedded documents or references
      Best for  |highly structured  |Evolving or semi-structured data
                |        data       |   

#_What is Schema?
A schema is basically the blueprint/structure of a database.
A schema is the official structure and rules of how data is organized inside a database.

#_CRUD :-
it is stands for basic operations performed on stored data.
(1) create, (2) read, (3) update, (4) delete

crud-operations|        MongoDB methods
---------------+----------------------------------
    create     |insertOne({document}), insertMany([document1, document2])
      read     |        findOne(), find()
    update     |updateOne(), updateMany(), replaceOne()
    delete     |        deleteOne(), deleteMany()

1. Create :-
- db.collectionName.insertOne({document})
- db.collectionName.insertMany([document1, document2])

2. Read :-
- db.collectionName.find({ field: value })
- db.collectionName.findOne({ field: value })

    #_Operators :-

    (i) Comparision operator :-

    MongoDB operator|Logical meaning
    ----------------+---------------
            $eq     |       ==
            $ne     |       !=
            $gt     |       >
            $gte    |       >=
            $lt     |       <
            $lte    |       <=

    (ii) Membership operator :-

    MongoDB operator|       Logical meaning
    ----------------+-----------------------------
            $in     |    value exists in list
            $nin    |value does not exists in list  

    (iii) Logical operator :-

    MongoDB operator|    Logical meaning
    ----------------+------------------------
           $and     |all condition must watch
           $or      | any condition can match

    (iv) Numeric operator :-
    - db.collectionName.find({
                                field: { $mod: [ divisor, remainder ] }
                            })

    (v) Array size operator :-
    - db.collectionName.find({
                                arrayFieldName: { $size: number }
                            })
                        
    (vi) Negation operator :-
            (a) $not = must not containing any 
                    e.g. - db.collectionName.find({
                                    fieldName: {
                                        $not: { operator: value }
                                }
                            })

            (b) $nor = nither this nor that
                    e.g. - db.collectionName.find({
                                $nor: [
                                    { condition1 },
                                    { condition2 },
                                    { condition3 }
                                ]
                            })

    (vii) Regex :-
    it is an operator that used to search the pattern of string/text
        (a) starts with :
                e.g. - db.users.find({
                            name: { $regex: "^A" }
                        })

        (b) ends with :
                e.g. - db.users.find({
                            name: { $regex: "n$" }
                        })

        (c) $options : case sensetive
                e.g. - db.collectionName.find({
                            fieldName: {
                                    $regex: "pattern",
                                    $options: "flag"
                            }
                        })
                
    (viii) Exper :-
        to compare two fields
            e.g. - db.collectionName.find({
                            $expr: {
                            operator: [ "$field1", "$field2" ]
                        }
                    })

                #_Exper operations : 

                    operator|  work
                    --------+--------
                      $add  |addition
                   $subtract| minus
                   $multiply|multiply
                    $divide |division
                      $mod  |remainder  

                    e.g. - db.collectionName.find({
                                    $expr: {
                                    operator: [ expression1, expression2 ]
                                }
                            })

#_Projection : 
    1 -> to include the field 
    0 -> to exlcude the field 
        e.g. - 
        db.collectionName.find(
                { queryCondition },
                { field1: 1, field2: 1, field3: 1 }
            )

#_Pagination :
    .sort : -1 -> decending order
             1 -> assending order
e.g. - db.collection.find(query)
                .sort({ field: 1/-1 })
                .skip()
                .limit()
                           
