---
bg: "tools.jpg"
layout: post
title:  "Data Structure - Linked List"
date:   2019-04-23 09:58:44 +1000
crawlertitle: "About Data Structure"
summary: "How to implement Linked List Algorithm in C#"
categories: posts
tags: ['Data Structure']
author: Masaab
---

#### Implementing Linked List Algorithm in C#

[Click here to get complete working code](https://github.com/masaab/DataStructure/tree/master/LinkedList)

*Insert Node at the end of the List:*

{% highlight C# %}
 public void InsertNodeAtEnd(Node node)
 {
     Node Temp = Head;

     while (Temp.Next != null)
     {
         Temp = Temp.Next;
     }
     Temp.Next = node;
 }
{% endhighlight %}

*Insert Node at the begining of the List:*

{% highlight C# %}
public void InsertNodeAtFirst(Node node)
 {
     node.Next = Head;
     Head = node;
 }
{% endhighlight %}

*Insert Node betwen the List:*

{% highlight C# %}
 public void GetPositionToInsertNode(Node node, int indexPosition)
 {
     int counter = 0;
     Node temp = Head;

     while (temp.Next != null)
     {
         if (indexPosition == counter)
         {
             node.Next = temp.Next;
             temp.Next = node;
             
             return;
         }
         temp = temp.Next;
         counter++;
     }
 }
{% endhighlight %}

*Traverse List*

{% highlight C# %}
while (Head.Next != null)
{
    Head = Head.Next;
    Debug.WriteLine(Head.Data);
}
{% endhighlight %}

*Delete First Node*

{% highlight C# %}
 public void DeleteFirstNode()
     => Head = Head.Next;
{% endhighlight %}

*Deletiing Last Node*

{% highlight C# %}
public void DeleteLastNode()
 {
     Node temp = Head;
     Node previousNode = Head;

     while (temp.Next != null)
     {
         previousNode = temp;
         temp = temp.Next;
     }
     previousNode.Next = null;
 }
{% endhighlight %}

*Delete Node From Middle*
{% highlight C# %}
 public void DeleteNodeFromMiddle(int nodeIndexPosition)
 {
     int counter = 0;
     Node temp = Head;
     Node previousNode = Head;
    
     while (temp.Next != null)
     {
         if (nodeIndexPosition == counter)
         {
             previousNode.Next = temp.Next;
             return;
         }
         previousNode = temp;
         temp = temp.Next;
         counter++;
     }
 }
{% endhighlight %}




