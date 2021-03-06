# Copyright CERN and copyright holders of ALICE O2. This software is distributed
# under the terms of the GNU General Public License v3 (GPL Version 3), copied
# verbatim in the file "COPYING".
#
# See http://alice-o2.web.cern.ch/license for full licensing information.
#
# In applying this license CERN does not waive the privileges and immunities
# granted to it by virtue of its status as an Intergovernmental Organization or
# submit itself to any jurisdiction.

add_subdirectory(workflow)

o2_add_test(itsmft
            PUBLIC_LINK_LIBRARIES O2::CTFWorkflow
                                  O2::ITSMFTReconstruction
	                          O2::DataFormatsITSMFT
            SOURCES test/test_ctf_io_itsmft.cxx
            COMPONENT_NAME ctf
            LABELS ctf)

o2_add_test(tpc
            PUBLIC_LINK_LIBRARIES O2::CTFWorkflow
                                  O2::TPCReconstruction
	                          O2::DataFormatsTPC
            SOURCES test/test_ctf_io_tpc.cxx
            COMPONENT_NAME ctf
            LABELS ctf)
          
o2_add_test(ft0
            PUBLIC_LINK_LIBRARIES O2::CTFWorkflow
                                  O2::FT0Reconstruction
	                          O2::DataFormatsFT0
            SOURCES test/test_ctf_io_ft0.cxx
            COMPONENT_NAME ctf
            LABELS ctf)
