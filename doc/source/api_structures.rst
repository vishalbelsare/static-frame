

Structures
===============================

Primary Containers
---------------------

The primary components of the StaticFrame library are the 1D :py:class:`Series` and the 2D :py:class:`Frame` and :py:class:`FrameGO`.

.. autoclass:: static_frame.Series

.. literalinclude:: api.py
   :language: python
   :start-after: start_series_a
   :end-before: end_series_a


.. autoclass:: static_frame.Frame

.. literalinclude:: api.py
   :language: python
   :start-after: start_frame_a
   :end-before: end_frame_a


.. autoclass:: static_frame.FrameGO

.. literalinclude:: api.py
   :language: python
   :start-after: start_framego_a
   :end-before: end_framego_a


Index Mappings
---------------------

Index mapping classes are used to map labels to ordinal positions on the :py:class:`Series`, :py:class:`Frame`, and :py:class:`FrameGO`.


.. autoclass:: static_frame.Index

.. literalinclude:: api.py
   :language: python
   :start-after: start_index_a
   :end-before: end_index_a


.. autoclass:: static_frame.IndexGO

.. literalinclude:: api.py
   :language: python
   :start-after: start_indexgo_a
   :end-before: end_indexgo_a


.. admonition:: Deviations from Pandas
    :class: Warning

    :py:class:`Index` and :py:class:`IndexGO` require that all labels are unique. Duplicated labels will raise an error in all cases. This deviates form Pandas, where Index objects permit duplicate labels. This also makes options like the ``verify_integrity`` argument to ``pd.Series.set_index`` and ``pd.DataFrame.set_index`` unnecessary.



Utility Objects
---------------------

The following objects are generally only created by internal clients, and thus are not fully documented here.

.. autoclass:: static_frame.TypeBlocks

.. autoclass:: static_frame.IterNode

.. autoclass:: static_frame.IterNodeDelegate

