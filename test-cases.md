# Engineering Test Plan

The following are planned checks for the CST simulation workflow. Their
status is **Not yet verified** unless the project team has performed and
recorded the test. These are simulation-quality checks, not clinical
validation tests.

  -----------------------------------------------------------------------------------
  ID             Test              Method               Evidence to    Status
                                                        retain         
  -------------- ----------------- -------------------- -------------- --------------
  TC-01          Geometry and      Review antenna, feed CST parameter  Not yet
                 units             and substrate        list and       verified
                                   dimensions           geometry view  

  TC-02          Materials         Confirm substrate    Material       Not yet
                                   and conductor        settings       verified
                                   assignments                         

  TC-03          Feed and port     Check port position, Port settings  Not yet
                                   orientation and      and model view verified
                                   excitation                          

  TC-04          Solver setup      Review boundaries,   Solver         Not yet
                                   frequency sweep and  settings       verified
                                   mesh                                

  TC-05          Solver completion Run the model and    Solver log /   Not yet
                                   review warnings      run status     verified

  TC-06          Patch resonance   Confirm resonance    Numerical      Not yet
                                   from exported        export and     verified
                                   S-parameter data     plot           

  TC-07          FSS curve         Confirm the meaning  Result-tree    Not yet
                 interpretation    of                   and port       verified
                                   `SZmin(1),Zmax(1)`   definition     
                                   in the result tree                  

  TC-08          Far-field         Identify which       Run ID and     Not yet
                 traceability      model/run produced   far-field      verified
                                   efficiency and       export         
                                   directivity                         

  TC-09          Result            Repeat a run with    Run settings   Not yet
                 reproducibility   unchanged settings   and result     verified
                                                        comparison     

  TC-10          FSS-versus-AMC    Run only after AMC   Matched        Pending AMC
                 comparison        model is completed;  comparison     design
                                   use equivalent       table          
                                   conditions                          
  -----------------------------------------------------------------------------------

## Acceptance principle

Record evidence before marking a test complete. If a test has not been
performed, keep its status as pending rather than claiming a pass.
