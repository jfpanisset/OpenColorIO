..
  SPDX-License-Identifier: CC-BY-4.0
  Copyright Contributors to the OpenColorIO Project.
  Do not edit! This file was automatically generated by share/docs/frozendoc.py.

.. py:class:: CDLTransform
   :module: PyOpenColorIO

   An implementation of the ASC Color Decision List (CDL), based on the ASC v1.2 specification.

   .. note::
      ​ If the config version is 1, negative values are clamped if the power is not 1.0. For config version 2 and higher, the negative handling is controlled by the CDL style.


   .. py:method:: CDLTransform.CreateFromFile(src: str, id: str) -> PyOpenColorIO.CDLTransform
      :module: PyOpenColorIO
      :staticmethod:

      Load the CDL from the src .cc or .ccc file. If a .ccc is used, the cccid must also be specified src must be an absolute path reference, no relative directory or envvar resolution is performed.


   .. py:method:: CDLTransform.__init__(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. __init__(self: PyOpenColorIO.CDLTransform) -> None

      2. __init__(self: PyOpenColorIO.CDLTransform, xml: str, direction: PyOpenColorIO.TransformDirection = <TransformDirection.TRANSFORM_DIR_FORWARD: 0>) -> None

      3. __init__(self: PyOpenColorIO.CDLTransform, slope: List[float[3]] = [1.0, 1.0, 1.0], offset: List[float[3]] = [0.0, 0.0, 0.0], power: List[float[3]] = [1.0, 1.0, 1.0], sat: float = 1.0, id: str = '', description: str = '', direction: PyOpenColorIO.TransformDirection = <TransformDirection.TRANSFORM_DIR_FORWARD: 0>) -> None


   .. py:method:: CDLTransform.__str__(self: PyOpenColorIO.CDLTransform) -> str
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.equals(self: PyOpenColorIO.CDLTransform, other: PyOpenColorIO.CDLTransform) -> bool
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getDescription(self: PyOpenColorIO.CDLTransform) -> str
      :module: PyOpenColorIO

      Deprecated. Use `getFormatMetadata`. First textual description of color correction (stored on the SOP). If there is already a description, the setter will replace it with the supplied text.


   .. py:method:: CDLTransform.getDirection(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformDirection
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getFormatMetadata(self: PyOpenColorIO.CDLTransform) -> PyOpenColorIO.FormatMetadata
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getID(self: PyOpenColorIO.CDLTransform) -> str
      :module: PyOpenColorIO

      rst:: **Metadata**


      Unique Identifier for this correction.


   .. py:method:: CDLTransform.getOffset(self: PyOpenColorIO.CDLTransform) -> List[float[3]]
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getPower(self: PyOpenColorIO.CDLTransform) -> List[float[3]]
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getSOP(self: PyOpenColorIO.CDLTransform) -> List[float[9]]
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getSat(self: PyOpenColorIO.CDLTransform) -> float
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getSatLumaCoefs(self: PyOpenColorIO.CDLTransform) -> List[float[3]]
      :module: PyOpenColorIO

      These are hard-coded, by spec, to r709.


   .. py:method:: CDLTransform.getSlope(self: PyOpenColorIO.CDLTransform) -> List[float[3]]
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getStyle(self: PyOpenColorIO.CDLTransform) -> PyOpenColorIO.CDLStyle
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getTransformType(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformType
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.getXML(self: PyOpenColorIO.CDLTransform) -> str
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setDescription(self: PyOpenColorIO.CDLTransform, description: str) -> None
      :module: PyOpenColorIO

      Deprecated. Use `getFormatMetadata`.


   .. py:method:: CDLTransform.setDirection(self: PyOpenColorIO.Transform, direction: PyOpenColorIO.TransformDirection) -> None
      :module: PyOpenColorIO

      Note that this only affects the evaluation and not the values stored in the object.


   .. py:method:: CDLTransform.setID(self: PyOpenColorIO.CDLTransform, id: str) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setOffset(self: PyOpenColorIO.CDLTransform, rgb: List[float[3]]) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setPower(self: PyOpenColorIO.CDLTransform, rgb: List[float[3]]) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setSOP(self: PyOpenColorIO.CDLTransform, vec9: List[float[9]]) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setSat(self: PyOpenColorIO.CDLTransform, sat: float) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setSlope(self: PyOpenColorIO.CDLTransform, rgb: List[float[3]]) -> None
      :module: PyOpenColorIO


   .. py:method:: CDLTransform.setStyle(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. setStyle(self: PyOpenColorIO.CDLTransform, style: PyOpenColorIO.CDLStyle) -> None

      Use CDL_ASC to clamp values to [0,1] per the ASC spec. Use NO_CLAMP to never clamp values (regardless of whether power is 1.0). The NO_CLAMP option passes negatives through unchanged (like the NEGATIVE_PASS_THRU style of :ref:`ExponentTransform`). The default style is CDL_NO_CLAMP.

      2. setStyle(self: PyOpenColorIO.CDLTransform, style: PyOpenColorIO.CDLStyle) -> None

      Use CDL_ASC to clamp values to [0,1] per the ASC spec. Use NO_CLAMP to never clamp values (regardless of whether power is 1.0). The NO_CLAMP option passes negatives through unchanged (like the NEGATIVE_PASS_THRU style of :ref:`ExponentTransform`). The default style is CDL_NO_CLAMP.


   .. py:method:: CDLTransform.setXML(self: PyOpenColorIO.CDLTransform, xml: str) -> None
      :module: PyOpenColorIO

      The default style is CDL_NO_CLAMP.


   .. py:method:: CDLTransform.validate(self: PyOpenColorIO.Transform) -> None
      :module: PyOpenColorIO

      Will throw if data is not valid.

