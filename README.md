# lammps_education_ch_win

Lammps ZTC for education (windows 10 (64 bit))
------------------------------------------------------------------------------
�� �C���X�g�[�����@

�� lammps
1. http://packages.lammps.org/windows.html ��HP��"64-bit Windows download area"���N���b�N����
2. LAMMPS-64bit-18Jun2019.exe ���_�E�����[�h���ĉ𓀂���
3. �f�B�t�H���g�̐ݒ�̂܂܍Ō�܂Ői�߂΂悢
�ȏ�� lammps �̃_�E�����[�h�Ɛݒ�͊����ł�

�E�`��\�t�g�ignuplot��Ovito�j
  gnuplot��Ovito�ɂ��Ă�web��ɗL�v�ȏ�񂪖L�x�ɂ���܂��̂ŁA���萔�����������܂����A����������Q�Ƃ�������
------------------------------------------------------------------------------
�� ���q���͊w�V�~�����[�V����

�� ���̓t�@�C���̃_�E�����[�h
  by-student-2017 �� lammps_education_ch_win (https://github.com/by-student-2017/lammps_education_ch_win) ������̓t�@�C�����_�E�����[�h���ĉ𓀂���B
  �E����[Clone or download]���N���b�N���Ă��������ƁADownload ZIP ���\������܂�
  
�� �V�~�����[�V�����̎��s
1. �e��̃t�H���_�̒��ɂ���run.bat���_�u���N���b�N����Όv�Z������
2. cfg��Ovito�ŊJ���΍\����������
3. plot�ƋL�ڂ̂���t�@�C�����_�u���N���b�N����ΐ}��������
  �I������ꍇ�͍�����ʂ�Enter������
  �� ���x���ړI�̒l�ɂȂ��Ă��邩�A�G�l���M�[�����̒l�ɂȂ��Ă��邩���m�F���Ă݂Ă�������
�� �ȏ�̎菇�́Adata.ch�ɂ��錴�q�̏�������������Α��̒Y�����f�ł����l�Ɍv�Z���\�ł�
�� plot���瓾����G(r)��X���⒆���q���̎������ʂƂ̔�r�ɗ��p������̂ł��Bmsd�͎��Ȋg�U�W�������߂�̂ɗ��p������̂ł�

�� tutorial_1_temp_and_press
  ���x�∳�͂�ς����Ƃ��̍\���̕ω��̃V�~�����[�V����
  in.lmp�t�@�C�����̉��� 298.0�̒l��ς���Ή��x���A300.0�̒l��ς���Έ��͂��ς��܂�
  variable    temp index 298.0 # K
  variable    pres index 300.0 # 30 MPa (bar units)

�� tutorial_2_strain
  �c�܂����Ƃ��̍\���̕ω��̃V�~�����[�V����
  in.lmp�t�@�C�����̉��� 0.05�̒l��ς���Έ������肪�s���܂��B���k�̏ꍇ�͕��̏����Ȓl�ɂ��Ă݂Ă��������B
  variable    Erate index 0.05 # 1/(0.5 fs), if Erate < 0.0 (compress)

�� tutorial_3_melt_and_cool
  ���x���グ����ɗ�₵���ꍇ�̍\���̕ω��̃V�~�����[�V����
  in.lmp�t�@�C�����̉���2000.0��1600.0, 1273.0�̒l��ς���Ɖ��x���ω����܂��B���̃t�@�C���̐ݒ�̗�ł́A2000.0 K �ȉ��ł̗��p�𐄏����܂�
  variable    tempm index 2200.0 # K (heat)
  variable    temph index 1600.0 # K (cool No.1)
  variable    tempc index 1273.0 # K (cool No.2)
�� ���̗�ł͂��܂茩���ڂ��ʔ�������܂��񂪁A���x�̒Ⴂ��ԂŒY�f���܂΂�ɔz�u����ƌ����̊j���ł��Ă����l�q���m�F���邱�Ƃ��ł��܂�

�� tutorial_4_thermal
  �M�`�����̌v�Z
  in.lmp�t�@�C�����̉��� 298.0�̒l��ς���Ή��x���A300.0�̒l��ς���Έ��͂��ς��܂�
  variable    temp index 298.0 # K
  variable    pres index 300.0 # 30 MPa (bar units)
  log.lammps�t�@�C���̍Ō�̕��ɁA�M�`�����iaverage conductivity�j���L�ڂ���Ă��܂��B���x�iK,�j�̌�ɋL�ڂ���Ă���̂͐����x�iNumber density�j�ł��Blog.lammps��Step���������Ă����ƁAv_Jx��v_Jy��v_Jz��0�Av_k11��v_k22��v_k33�͂����ނˈ��̒l�ɂȂ��Ă��邩���m�F���Ă݂Ă�������
�� ����͒萫�I�܂��͔���ʓI�ȔM�`�����̕]���Ƃ��ė��p����܂�

�� tutorial_5_viscosity
  �S�����i�S���W���A�S�x�Ƃ��Ă΂��j�̌v�Z
  in.lmp�t�@�C�����̉��� 898.0�̒l��ς���Ή��x���A10.0�̒l��ς���Έ��͂��ς��܂�
  variable    temp index 898.0 # K
  variable    pres index 10.0 # 1.0 MPa (bar units)
  log.lammps�t�@�C���̍Ō�̕��ɁA�S�����iaverage viscosity�j���L�ڂ���Ă��܂��B���x�iK,�j�̌�ɋL�ڂ���Ă���̂͐����x�iNumber density�j�ł��Blog.lammps��Step���������Ă����ƁA"v_pxy v_pxz v_pyz v_v11 v_v22 v_v33"�͂����ނˈ��̒l�ɂȂ��Ă��邩���m�F���Ă݂Ă�������
�� ����͒萫�I�܂��͔���ʓI�ȔS�����̕]���Ƃ��ė��p����܂�

�E �Y�f�Ɛ��f�Ǝ_�f�Ōv�Z�������ꍇ�́AreaxFF��p����Ɖ\�ɂȂ�B�|�e���V�����̃t�@�C���̏��́ANIST�ihttps://www.ctcms.nist.gov/potentials/system/C/#C-H-O�j�ɋL�ڂ���Ă���BNIST�Ɍv�Z����Ă���|�e���V������p���āA��L�̓��̓t�@�C���������������C-H-O�����łȂ�C-Si��C-Cu, C-Fe, B-C-N�Ƃ��������f�̑g�ݍ��킹�ł��萫�I�܂��͔���ʓI�ȗ\�����\�ɂȂ�B
------------------------------------------------------------------------------


