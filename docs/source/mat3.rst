.. default-domain:: C

mat3
====

Header: cglm/mat3.h

Table of contents (clik func/macro to go):
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Macros:

1. GLM_MAT3_IDENTITY_INIT
#. GLM_MAT3_ZERO_INIT
#. GLM_MAT3_IDENTITY
#. GLM_MAT3_ZERO
#. glm_mat3_dup(mat, dest)

Functions:

1. :c:func:`glm_mat3_copy`
#. :c:func:`glm_mat3_identity`
#. :c:func:`glm_mat3_mul`
#. :c:func:`glm_mat3_transpose_to`
#. :c:func:`glm_mat3_transpose`
#. :c:func:`glm_mat3_mulv`
#. :c:func:`glm_mat3_scale`
#. :c:func:`glm_mat3_det`
#. :c:func:`glm_mat3_inv`
#. :c:func:`glm_mat3_swap_col`
#. :c:func:`glm_mat3_swap_row`

Functions documentation
~~~~~~~~~~~~~~~~~~~~~~~

.. c:function:: void  glm_mat3_copy(mat3 mat, mat3 dest)

    copy mat3 to another one (dest).

    Parameters:
      | *[in]*  **mat**   source
      | *[out]* **dest**  destination

.. c:function:: void  glm_mat3_identity(mat3 mat)

    copy identity mat3 to mat, or makes mat to identiy

    Parameters:
      | *[out]* **mat**  matrix

.. c:function:: void  glm_mat3_mul(mat3 m1, mat3 m2, mat3 dest)

    multiply m1 and m2 to dest
    m1, m2 and dest matrices can be same matrix, it is possible to write this:

    .. code-block:: c

       mat3 m = GLM_MAT3_IDENTITY_INIT;
       glm_mat3_mul(m, m, m);

    Parameters:
      | *[in]*  **m1**    left matrix
      | *[in]*  **m2**    right matrix
      | *[out]* **dest**  destination matrix

.. c:function:: void  glm_mat3_transpose_to(mat3 m, mat3 dest)

    transpose mat4 and store in dest
    source matrix will not be transposed unless dest is m

    Parameters:
      | *[in]*  **mat**   source
      | *[out]* **dest**  destination

.. c:function:: void  glm_mat3_transpose(mat3 m)

    tranpose mat3 and store result in same matrix

    Parameters:
      | *[in]*  **mat**   source
      | *[out]* **dest**  destination

.. c:function:: void  glm_mat3_mulv(mat3 m, vec3 v, vec3 dest)

    multiply mat4 with vec4 (column vector) and store in dest vector

    Parameters:
      | *[in]*  **mat**   mat3 (left)
      | *[in]*  **v**     vec3 (right, column vector)
      | *[out]* **dest**  destination (result, column vector)

.. c:function:: void  glm_mat3_scale(mat3 m, float s)

    multiply matrix with scalar

    Parameters:
      | *[in, out]* **mat**   matrix
      | *[in]*      **dest**  scalar

.. c:function:: float  glm_mat3_det(mat3 mat)

    returns mat3 determinant

    Parameters:
      | *[in]*  **mat**   matrix

    Returns:
        mat3 determinant

.. c:function:: void glm_mat3_inv(mat3 mat, mat3 dest)

    inverse mat3 and store in dest

    Parameters:
      | *[in]*  **mat**  matrix
      | *[out]* **dest** destination (inverse matrix)

.. c:function:: void  glm_mat3_swap_col(mat3 mat, int col1, int col2)

    swap two matrix columns

    Parameters:
      | *[in, out]*  **mat**   matrix
      | *[in]*       **col1**  col1
      | *[in]*       **col2**  col2

.. c:function:: void  glm_mat3_swap_row(mat3 mat, int row1, int row2)

    swap two matrix rows

    Parameters:
      | *[in, out]*  **mat**   matrix
      | *[in]*       **row1**  row1
      | *[in]*       **row2**  row2