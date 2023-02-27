http://mikehadlow.blogspot.com/2018/11/decoupling-architecture-and-teams.html

Why productivity of developers decrease with complexity of system ?
1. As developer cognitive attention is limited and remembering all the components become difficult. 
2. Developers learn to work in a minimum-impact style of work-arounds and duplication rather than factoring out commonalities and creating abstractions and generalisations. 
3. This feeds back into system complexity, further amplifying these negative trends

How to solve above problem ?
1. This can be seen quite obviously if you consider a tree. _Each small part of the tree looks like a small tree_.

Properties of decouple system
-   Obeys a shared communication protocol. Have API defined.
-   Only shares state via a clear contract with other nodes. Meaning state of one class/package/module/component is shared only throug it's return value.
-   Does not require implementation knowledge to communicate. Doesn't/Shouldn't now what are the implement details it all about obeying contract. 
-   Versioned and deployed independently. 

Properties of decoupled teams
* Sub team should look like complete organization. From tree metaphor.
* The internal processes and communication of the team should not be a concern outside the team.
* How the team implements software shouldn't be concern outside.
* Teams should communicate with the wider organisation about external concerns: common protocols, features, service levels and resourcing.
