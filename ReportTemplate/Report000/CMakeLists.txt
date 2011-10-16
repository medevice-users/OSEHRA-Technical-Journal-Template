project(HowToWriteTechnicalReport)


#
#  Copy LaTeX files to the binary build directory
#
#  This LATEX_FILES variable is populated in the top CMakeLists.txt file
#
file(
  COPY  ${LATEX_FILES}
  DESTINATION ${HowToWriteTechnicalReport_BINARY_DIR}
  )


#
#  Copy MUMPS files to the binary build directory
#  to make easier to source them as code snippets.
#
#  This MUMPS_FILES variable is populated in the top CMakeLists.txt file
#
file(
  COPY  ${MUMPS_FILES}
  DESTINATION ${HowToWriteTechnicalReport_BINARY_DIR}
  )


add_latex_document( HowToWriteTechnicalReport.tex
  IMAGE_DIRS ../Art
  DEFAULT_PDF
  )

