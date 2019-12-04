# lammps_education_ch_win

Lammps ZTC for education (windows 10 (64 bit))
------------------------------------------------------------------------------
■ インストール方法

□ lammps
1. http://packages.lammps.org/windows.html のHPで"64-bit Windows download area"をクリックする
2. LAMMPS-64bit-18Jun2019.exe をダウンロードして解凍する
3. ディフォルトの設定のまま最後まで進めばよい
以上で lammps のダウンロードと設定は完了です

・描画ソフト（gnuplotとOvito）
  gnuplotとOvitoについてはweb上に有益な情報が豊富にありますので、お手数をおかけしますが、そちらをご参照ください
------------------------------------------------------------------------------
■ 分子動力学シミュレーション

□ 入力ファイルのダウンロード
  by-student-2017 の lammps_education_ch_win (https://github.com/by-student-2017/lammps_education_ch_win) から入力ファイルをダウンロードして解凍する。
  右側の[Clone or download]をクリックしていただくと、Download ZIP が表示されます
  
□ シミュレーションの実行
1. 各種のフォルダの中にあるrun.batをダブルクリックすれば計算が走る
2. cfgをOvitoで開けば構造が得られる
3. plotと記載のあるファイルをダブルクリックすれば図が得られる
  終了する場合は黒い画面でEnterを押す
  ※ 温度が目的の値になっているか、エネルギーが一定の値になっているかを確認してみてください
※ 以上の手順は、data.chにある原子の情報を書きかえれば他の炭化水素でも同様に計算が可能です
※ plotから得られるG(r)はX線や中性子線の実験結果との比較に利用するものです。msdは自己拡散係数を求めるのに利用するものです

□ tutorial_1_temp_and_press
  温度や圧力を変えたときの構造の変化のシミュレーション
  in.lmpファイル中の下の 298.0の値を変えれば温度が、300.0の値を変えれば圧力が変わります
  variable    temp index 298.0 # K
  variable    pres index 300.0 # 30 MPa (bar units)

□ tutorial_2_strain
  歪ませたときの構造の変化のシミュレーション
  in.lmpファイル中の下の 0.05の値を変えれば引っ張りが行われます。圧縮の場合は負の小さな値にしてみてください。
  variable    Erate index 0.05 # 1/(0.5 fs), if Erate < 0.0 (compress)

□ tutorial_3_melt_and_cool
  温度を上げた後に冷やした場合の構造の変化のシミュレーション
  in.lmpファイル中の下の2000.0や1600.0, 1273.0の値を変えると温度が変化します。このファイルの設定の例では、2000.0 K 以下での利用を推奨します
  variable    tempm index 2200.0 # K (heat)
  variable    temph index 1600.0 # K (cool No.1)
  variable    tempc index 1273.0 # K (cool No.2)
※ この例ではあまり見た目が面白くありませんが、密度の低い状態で炭素をまばらに配置すると結晶の核ができていく様子を確認することができます

□ tutorial_4_thermal
  熱伝導率の計算
  in.lmpファイル中の下の 298.0の値を変えれば温度が、300.0の値を変えれば圧力が変わります
  variable    temp index 298.0 # K
  variable    pres index 300.0 # 30 MPa (bar units)
  log.lammpsファイルの最後の方に、熱伝導率（average conductivity）が記載されています。温度（K,）の後に記載されているのは数密度（Number density）です。log.lammpsでStep数が増えていくと、v_Jxやv_Jyやv_Jzは0、v_k11やv_k22やv_k33はおおむね一定の値になっているかも確認してみてください
※ これは定性的または半定量的な熱伝導率の評価として利用されます

□ tutorial_5_viscosity
  粘性率（粘性係数、粘度とも呼ばれる）の計算
  in.lmpファイル中の下の 898.0の値を変えれば温度が、10.0の値を変えれば圧力が変わります
  variable    temp index 898.0 # K
  variable    pres index 10.0 # 1.0 MPa (bar units)
  log.lammpsファイルの最後の方に、粘性率（average viscosity）が記載されています。温度（K,）の後に記載されているのは数密度（Number density）です。log.lammpsでStep数が増えていくと、"v_pxy v_pxz v_pyz v_v11 v_v22 v_v33"はおおむね一定の値になっているかも確認してみてください
※ これは定性的または半定量的な粘性率の評価として利用されます

・ 炭素と水素と酸素で計算したい場合は、reaxFFを用いると可能になる。ポテンシャルのファイルの情報は、NIST（https://www.ctcms.nist.gov/potentials/system/C/#C-H-O）に記載されている。NISTに計算されているポテンシャルを用いて、上記の入力ファイルを書きかえればC-H-OだけでなくC-SiやC-Cu, C-Fe, B-C-Nといった元素の組み合わせでも定性的または半定量的な予測が可能になる。
------------------------------------------------------------------------------


