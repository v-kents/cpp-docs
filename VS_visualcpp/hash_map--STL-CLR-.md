---
title: "hash_map (STL-CLR)"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
H1: hash_map (STL/CLR)
ms.assetid: c3cfc69b-04c6-42ae-a30e-0eda953fe883
caps.latest.revision: 20
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# hash_map (STL-CLR)
The template class describes an object that controls a varying-length sequence of elements that has bidirectional access. You use the container `hash_map` to manage a sequence of elements as a hash table, each table entry storing a bidirectional linked list of nodes, and each node storing one element. An element consists of a key, for ordering the sequence, and a mapped value, which goes along for the ride.  
  
 In the description below, `GValue` is the same as:  
  
 `Microsoft::VisualC::StlClr::GenericPair<GKey, GMapped>`  
  
 where:  
  
 `GKey` is the same as `Key` unless the latter is a ref type, in which case it is `Key^`  
  
 `GMapped` is the same as `Mapped` unless the latter is a ref type, in which case it is `Mapped^`  
  
## Syntax  
  
```  
template<typename Key,  
    typename Mapped>  
    ref class hash_map  
        :   public  
        System::ICloneable,  
        System::Collections::IEnumerable,  
        System::Collections::ICollection,  
        System::Collections::Generic::IEnumerable<GValue>,  
        System::Collections::Generic::ICollection<GValue>,  
        System::Collections::Generic::IList<GValue>,  
        System::Collections::Generic::IDictionary<Gkey, GMapped>,  
        Microsoft::VisualC::StlClr::IHash<Gkey, GValue>  
    { ..... };  
```  
  
#### Parameters  
 Key  
 The type of the key component of an element in the controlled sequence.  
  
 Mapped  
 The type of the additional component of an element in the controlled sequence.  
  
## Members  
  
|Type Definition|Description|  
|---------------------|-----------------|  
|[hash_map::const_iterator (STL/CLR)](../VS_visualcpp/hash_map--const_iterator--STL-CLR-.md)|The type of a constant iterator for the controlled sequence.|  
|[hash_map::const_reference (STL/CLR)](../VS_visualcpp/hash_map--const_reference--STL-CLR-.md)|The type of a constant reference to an element.|  
|[hash_map::const_reverse_iterator (STL/CLR)](../VS_visualcpp/hash_map--const_reverse_iterator--STL-CLR-.md)|The type of a constant reverse iterator for the controlled sequence.|  
|[hash_map::difference_type (STL/CLR)](../VS_visualcpp/hash_map--difference_type--STL-CLR-.md)|The type of a (possibly signed) distance between two elements.|  
|[hash_map::generic_container (STL/CLR)](../VS_visualcpp/hash_map--generic_container--STL-CLR-.md)|The type of the generic interface for the container.|  
|[hash_map::generic_iterator (STL/CLR)](../VS_visualcpp/hash_map--generic_iterator--STL-CLR-.md)|The type of an iterator for the generic interface for the container.|  
|[hash_map::generic_reverse_iterator (STL/CLR)](../VS_visualcpp/hash_map--generic_reverse_iterator--STL-CLR-.md)|The type of a reverse iterator for the generic interface for the container.|  
|[hash_map::generic_value (STL/CLR)](../VS_visualcpp/hash_map--generic_value--STL-CLR-.md)|The type of an element for the generic interface for the container.|  
|[hash_map::hasher (STL/CLR)](../VS_visualcpp/hash_map--hasher--STL-CLR-.md)|The hashing delegate for a key.|  
|[hash_map::iterator (STL/CLR)](../VS_visualcpp/hash_map--iterator--STL-CLR-.md)|The type of an iterator for the controlled sequence.|  
|[hash_map::key_compare (STL/CLR)](../VS_visualcpp/hash_map--key_compare--STL-CLR-.md)|The ordering delegate for two keys.|  
|[hash_map::key_type (STL/CLR)](../VS_visualcpp/hash_map--key_type--STL-CLR-.md)|The type of an ordering key.|  
|[hash_map::mapped_type (STL/CLR)](../VS_visualcpp/hash_map--mapped_type--STL-CLR-.md)|The type of the mapped value associated with each key.|  
|[hash_map::reference (STL/CLR)](../VS_visualcpp/hash_map--reference--STL-CLR-.md)|The type of a reference to an element.|  
|[hash_map::reverse_iterator (STL/CLR)](../VS_visualcpp/hash_map--reverse_iterator--STL-CLR-.md)|The type of a reverse iterator for the controlled sequence.|  
|[hash_map::size_type (STL/CLR)](../VS_visualcpp/hash_map--size_type--STL-CLR-.md)|The type of a (non-negative) distance between two elements.|  
|[hash_map::value_compare (STL/CLR)](../VS_visualcpp/hash_map--value_compare--STL-CLR-.md)|The ordering delegate for two element values.|  
|[hash_map::value_type (STL/CLR)](../VS_visualcpp/hash_map--value_type--STL-CLR-.md)|The type of an element.|  
  
|Member Function|Description|  
|---------------------|-----------------|  
|[hash_map::begin (STL/CLR)](../VS_visualcpp/hash_map--begin--STL-CLR-.md)|Designates the beginning of the controlled sequence.|  
|[hash_map::bucket_count (STL/CLR)](../VS_visualcpp/hash_map--bucket_count--STL-CLR-.md)|Counts the number of buckets.|  
|[hash_map::clear (STL/CLR)](../VS_visualcpp/hash_map--clear--STL-CLR-.md)|Removes all elements.|  
|[hash_map::count (STL/CLR)](../VS_visualcpp/hash_map--count--STL-CLR-.md)|Counts elements matching a specified key.|  
|[hash_map::empty (STL/CLR)](../VS_visualcpp/hash_map--empty--STL-CLR-.md)|Tests whether no elements are present.|  
|[hash_map::end (STL/CLR)](../VS_visualcpp/hash_map--end--STL-CLR-.md)|Designates the end of the controlled sequence.|  
|[hash_map::equal_range (STL/CLR)](../VS_visualcpp/hash_map--equal_range--STL-CLR-.md)|Finds range that matches a specified key.|  
|[hash_map::erase (STL/CLR)](../VS_visualcpp/hash_map--erase--STL-CLR-.md)|Removes elements at specified positions.|  
|[hash_map::find (STL/CLR)](../VS_visualcpp/hash_map--find--STL-CLR-.md)|Finds an element that matches a specified key.|  
|[hash_map::hash_delegate (STL/CLR)](../VS_visualcpp/hash_map--hash_delegate--STL-CLR-.md)|Copies the hashing delegate for a key.|  
|[hash_map::hash_map (STL/CLR)](../VS_visualcpp/hash_map--hash_map--STL-CLR-.md)|Constructs a container object.|  
|[hash_map::insert (STL/CLR)](../VS_visualcpp/hash_map--insert--STL-CLR-.md)|Adds elements.|  
|[hash_map::key_comp (STL/CLR)](../VS_visualcpp/hash_map--key_comp--STL-CLR-.md)|Copies the ordering delegate for two keys.|  
|[hash_map::load_factor (STL/CLR)](../VS_visualcpp/hash_map--load_factor--STL-CLR-.md)|Counts the average elements per bucket.|  
|[hash_map::lower_bound (STL/CLR)](../VS_visualcpp/hash_map--lower_bound--STL-CLR-.md)|Finds beginning of range that matches a specified key.|  
|[hash_map::make_value (STL/CLR)](../VS_visualcpp/hash_map--make_value--STL-CLR-.md)|Constructs a value object.|  
|[hash_map::max_load_factor (STL/CLR)](../VS_visualcpp/hash_map--max_load_factor--STL-CLR-.md)|Gets or sets the maximum elements per bucket.|  
|[hash_map::rbegin (STL/CLR)](../VS_visualcpp/hash_map--rbegin--STL-CLR-.md)|Designates the beginning of the reversed controlled sequence.|  
|[hash_map::rehash (STL/CLR)](../VS_visualcpp/hash_map--rehash--STL-CLR-.md)|Rebuilds the hash table.|  
|[hash_map::rend (STL/CLR)](../VS_visualcpp/hash_map--rend--STL-CLR-.md)|Designates the end of the reversed controlled sequence.|  
|[hash_map::size (STL/CLR)](../VS_visualcpp/hash_map--size--STL-CLR-.md)|Counts the number of elements.|  
|[hash_map::swap (STL/CLR)](../VS_visualcpp/hash_map--swap--STL-CLR-.md)|Swaps the contents of two containers.|  
|[hash_map::to_array (STL/CLR)](../VS_visualcpp/hash_map--to_array--STL-CLR-.md)|Copies the controlled sequence to a new array.|  
|[hash_map::upper_bound (STL/CLR)](../VS_visualcpp/hash_map--upper_bound--STL-CLR-.md)|Finds end of range that matches a specified key.|  
|[hash_map::value_comp (STL/CLR)](../VS_visualcpp/hash_map--value_comp--STL-CLR-.md)|Copies the ordering delegate for two element values.|  
  
|Operator|Description|  
|--------------|-----------------|  
|[hash_map::operator= (STL/CLR)](../VS_visualcpp/hash_map--operator=--STL-CLR-.md)|Replaces the controlled sequence.|  
|[hash_map::operator(STL/CLR)](../VS_visualcpp/hash_map--operator-STL-CLR-.md)|Maps a key to its associated mapped value.|  
  
## Interfaces  
  
|Interface|Description|  
|---------------|-----------------|  
|<xref:System.ICloneable?qualifyHint=False>|Duplicate an object.|  
|<xref:System.Collections.IEnumerable?qualifyHint=False>|Sequence through elements.|  
|<xref:System.Collections.ICollection?qualifyHint=False>|Maintain group of elements.|  
|<xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>|Sequence through typed elements.|  
|<xref:System.Collections.Generic.ICollection`1?qualifyHint=False>|Maintain group of typed elements.|  
|<xref:System.Collections.Generic.IDictionary`2?qualifyHint=False>|Maintain group of {key, value} pairs.|  
|IHash<Key, Value>|Maintain generic container.|  
  
## Remarks  
 The object allocates and frees storage for the sequence it controls as individual nodes in a bidirectional linked list. To speed access, the object also maintains a varying-length array of pointers into the list (the hash table), effectively managing the whole list as a sequence of sublists, or buckets. It inserts elements into a bucket that it keeps ordered by altering the links between nodes, never by copying the contents of one node to another. That means you can insert and remove elements freely without disturbing remaining elements.  
  
 The object orders each bucket it controls by calling a stored delegate object of type [hash_set::key_compare (STL/CLR)](../VS_visualcpp/hash_set--key_compare--STL-CLR-.md). You can specify the stored delegate object when you construct the hash_set; if you specify no delegate object, the default is the comparison `operator<=(key_type, key_type)`.  
  
 You access the stored delegate object by calling the member function [hash_set::key_comp (STL/CLR)](../VS_visualcpp/hash_set--key_comp--STL-CLR-.md)`()`. Such a delegate object must define equivalent ordering between keys of type [hash_set::key_type (STL/CLR)](../VS_visualcpp/hash_set--key_type--STL-CLR-.md). That means, for any two keys `X` and `Y`:  
  
 `key_comp()(X, Y)` returns the same Boolean result on every call.  
  
 If `key_comp()(X, Y) && key_comp()(Y, X)` is true, then `X` and `Y` are said to have equivalent ordering.  
  
 Any ordering rule that behaves like `operator<=(key_type, key_type)`, `operator>=(key_type, key_type)` or `operator==(key_type, key_type)` defines eqivalent ordering.  
  
 Note that the container ensures only that elements whose keys have equivalent ordering (and which hash to the same integer value) are adjacent within a bucket. Unlike template class [hash_multimap (STL/CLR)](../VS_visualcpp/hash_multimap--STL-CLR-.md), an object of template class `hash_map` ensures that keys for all elements are unique. (No two keys have equivalent ordering.)  
  
 The object determines which bucket should contain a given ordering key by calling a stored delegate object of type [hash_set::hasher (STL/CLR)](../VS_visualcpp/hash_set--hasher--STL-CLR-.md). You access this stored object by calling the member function [hash_set::hash_delegate (STL/CLR)](../VS_visualcpp/hash_set--hash_delegate--STL-CLR-.md)`()` to obtain an integer value that depends on the key value. You can specify the stored delegate object when you construct the hash_set; if you specify no delegate object, the default is the function `System::Object::hash_value(key_type)`. That means, for any keys `X` and `Y`:  
  
 `hash_delegate()(X)` returns the same integer result on every call.  
  
 If `X` and `Y` have equivalent ordering, then `hash_delegate()(X)` should return the same integer result as `hash_delegate()(Y)`.  
  
 Each element contains a separate key and a mapped value. The sequence is represented in a way that permits lookup, insertion, and removal of an arbitrary element with a number of operations that is independent of the number of elements in the sequence (constant time) -- at least in the best of cases. Moreover, inserting an element invalidates no iterators, and removing an element invalidates only those iterators which point at the removed element.  
  
 If hashed values are not uniformly distributed, however, a hash table can degenerate. In the extreme -- for a hash function that always returns the same value -- lookup, insertion, and removal are proportional to the number of elements in the sequence (linear time). The container endeavors to choose a reasonable hash function, mean bucket size, and hash-table size (total number of buckets), but you can override any or all of these choices. See, for example, the functions [hash_set::max_load_factor (STL/CLR)](../VS_visualcpp/hash_set--max_load_factor--STL-CLR-.md) and [hash_set::rehash (STL/CLR)](../VS_visualcpp/hash_set--rehash--STL-CLR-.md).  
  
 A hash_map supports bidirectional iterators, which means you can step to adjacent elements given an iterator that designates an element in the controlled sequence. A special head node corresponds to the iterator returned by [hash_map::end (STL/CLR)](../VS_visualcpp/hash_map--end--STL-CLR-.md)`()`. You can decrement this iterator to reach the last element in the controlled sequence, if present. You can increment a hash_map iterator to reach the head node, and it will then compare equal to `end()`. But you cannot dereference the iterator returned by `end()`.  
  
 Note that you cannot refer to a hash_map element directly given its numerical position -- that requires a random-access iterator.  
  
 A hash_map iterator stores a handle to its associated hash_map node, which in turn stores a handle to its associated container. You can use iterators only with their associated container objects. A hash_map iterator remains valid so long as its associated hash_map node is associated with some hash_map. Moreover, a valid iterator is dereferencable -- you can use it to access or alter the element value it designates -- so long as it is not equal to `end()`.  
  
 Erasing or removing an element calls the destructor for its stored value. Destroying the container erases all elements. Thus, a container whose element type is a ref class ensures that no elements outlive the container. Note, however, that a container of handles does `not` destroy its elements.  
  
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_map](../VS_visualcpp/hash_map--STL-CLR-.md)   
 [hash_multiset (STL/CLR)](../VS_visualcpp/hash_multiset--STL-CLR-.md)   
 [hash_set (STL/CLR)](../VS_visualcpp/hash_set--STL-CLR-.md)   
 [map (STL/CLR)](../VS_visualcpp/map--STL-CLR-.md)   
 [multimap (STL/CLR)](../VS_visualcpp/multimap--STL-CLR-.md)   
 [multiset (STL/CLR)](../VS_visualcpp/multiset--STL-CLR-.md)   
 [set (STL/CLR)](../VS_visualcpp/set--STL-CLR-.md)   
 [STL/CLR Library Reference](../VS_visualcpp/STL-CLR-Library-Reference.md)