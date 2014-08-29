Document Traversal
======================

::

  template<class Args...>
  struct document_traversal
  {
    template<class XMLElement, class Context>
    static bool load_document(XMLElement const & xml_element_svg, Context & context);

    template<class RefArgs...>
    struct load_referenced_element
    {
      template<class XMLElement, class Context>
      static bool load(XMLElement const & xml_element, Context & parent_context);
    };
  };

Named class template parameters

  ``ignored_elements`` and ``processed_elements``

    ���� �� ���� ���������� ������ ���� �����, ����� ���������� ����� �������� SVG ��������������. 
    �������� ��������� - model of `Associative Sequence`_, �������� ``boost::mpl::set``,
    ���������� ���� ���������.

    ���� ����� ``processed_elements``, �� ��������� �������������� ������ �������������� ����������,
    ���� ``ignored_elements``, �� �������������� ��� ��������, ����� �������������.

  ``context_factories``

    