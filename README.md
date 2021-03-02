# HW2_2
        class Program
        {
            static void Main(string[] args)
            {

            }
            public class Node
            {
                public int Value { get; set; }
                public Node NextNode { get; set; }
                public Node PrevNode { get; set; }
            }
            public interface ILinkedList
            {
                int GetCount(); // возвращает количество элементов в списке
                void AddNode(int value);  // добавляет новый элемент списка
                void AddNodeAfter(Node node, int value); // добавляет новый элемент списка после определённого элемента
                void RemoveNode(int index); // удаляет элемент по порядковому номеру
                void RemoveNode(Node node); // удаляет указанный элемент
                Node FindNode(int searchValue); // ищет элемент по его значению
            }
            public class LinkedList : ILinkedList
            {
                private int _count = 0;
                private Node _startNode;
                private Node _endNode;
                private Node _first;
                private Node _second;
                                public void AddNode(int value)
                {
                    if (_startNode == null)
                    {
                        _startNode = new Node { Value = value };
                        _endNode = _startNode;
                    }
                    else
                    {
                        _first = _startNode;
                        while (_first.NextNode != null)
                        {
                            _first = _first.NextNode;
                        }
                        _endNode = new Node { Value = value, PrevNode = _first };
                        _first.NextNode = _endNode;
                    }

                    _count++;
                }
               }
              }

/*Требуется реализовать класс двусвязного списка и операции
вставки, удаления и поиска элемента 
в нём в соответствии с интерфейсом.*/
