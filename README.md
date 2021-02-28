# HW2_2

using System;

namespace example2
{
    public class Node
        {
        public int Value { get; set; }
        public Node NextItem { get; set; } //NextNode
        public Node PrevItem { get; set; } //PrevNode

        
        
        public interface ILinkedList
        {
            void AddNode(int value) //добавляет новый элемент списка
                { 

                }
            void AddNodeAfter(Node node, int value)  //добавляет новый элемент списка после определенного элемента
            {
                var newNode = new Node { Value = value }; 
                var nextItem = node.NextItem; 
                var prevItem = node.PrevItem;
                node.NextItem = newNode;
                node.PrevItem = newNode;
                newNode.NextItem = nextItem;
                newNode.PrevItem = prevItem;
            }
            void RemoveNode(Node node)//удаляет указанный элемент 
                {

                }
            void RemoveNode(int node) //удаляет элемент по порядковому номеру
                {

                }
            Node FindNode(int searchValue) //ищет элемент по его значению
                {
            
                }
        }
    }
}
/*Требуется реализовать класс двусвязного списка и операции
вставки, удаления и поиска элемента 
в нём в соответствии с интерфейсом.*/
