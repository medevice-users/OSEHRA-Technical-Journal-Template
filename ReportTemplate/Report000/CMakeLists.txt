project(CPRS-Technical-Article)


#
#  Copy LaTeX files to the binary build directory
#
#  This LATEX_FILES variable is populated in the top CMakeLists.txt file
#
file(
  COPY  ${LATEX_FILES}
  DESTINATION ${CPRS-Technical-Article_BINARY_DIR}
  )


#
#  Copy MUMPS files to the binary build directory
#  to make easier to source them as code snippets.
#
#  This MUMPS_FILES variable is populated in the top CMakeLists.txt file
#
file(
  COPY  ${MUMPS_FILES}
  DESTINATION ${CPRS-Technical-Article_BINARY_DIR}
  )


add_latex_document( CPRS-Technical-Article.tex
  IMAGE_DIRS ../Art
  DEFAULT_PDF
  )

