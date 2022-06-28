# Local Moran statistics are stable

    Code
      (df_local_i <- ww_local_moran_i(guerry_modeled, crime_pers, predictions, ctg,
        wts))
    Output
      # A tibble: 85 x 4
         .metric       .estimator .estimate                                   geometry
         <chr>         <chr>          <dbl>                             <MULTIPOLYGON>
       1 local_moran_i standard      0.530  (((381847 1762775, 381116 1763059, 379972~
       2 local_moran_i standard      0.858  (((381847 1762775, 381116 1763059, 379972~
       3 local_moran_i standard      0.759  (((381847 1762775, 381116 1763059, 379972~
       4 local_moran_i standard      0.732  (((381847 1762775, 381116 1763059, 379972~
       5 local_moran_i standard      0.207  (((381847 1762775, 381116 1763059, 379972~
       6 local_moran_i standard      0.860  (((381847 1762775, 381116 1763059, 379972~
       7 local_moran_i standard      0.692  (((381847 1762775, 381116 1763059, 379972~
       8 local_moran_i standard      1.69   (((381847 1762775, 381116 1763059, 379972~
       9 local_moran_i standard     -0.0109 (((381847 1762775, 381116 1763059, 379972~
      10 local_moran_i standard      0.710  (((381847 1762775, 381116 1763059, 379972~
      # ... with 75 more rows

---

    Code
      (df_local_i_p <- ww_local_moran_pvalue(guerry_modeled, crime_pers, predictions,
        ctg, wts))
    Output
      # A tibble: 85 x 4
         .metric            .estimator .estimate                              geometry
         <chr>              <chr>          <dbl>                        <MULTIPOLYGON>
       1 local_moran_pvalue standard     0.194   (((381847 1762775, 381116 1763059, 3~
       2 local_moran_pvalue standard     0.0109  (((381847 1762775, 381116 1763059, 3~
       3 local_moran_pvalue standard     0.0123  (((381847 1762775, 381116 1763059, 3~
       4 local_moran_pvalue standard     0.0600  (((381847 1762775, 381116 1763059, 3~
       5 local_moran_pvalue standard     0.120   (((381847 1762775, 381116 1763059, 3~
       6 local_moran_pvalue standard     0.0463  (((381847 1762775, 381116 1763059, 3~
       7 local_moran_pvalue standard     0.243   (((381847 1762775, 381116 1763059, 3~
       8 local_moran_pvalue standard     0.0641  (((381847 1762775, 381116 1763059, 3~
       9 local_moran_pvalue standard     0.821   (((381847 1762775, 381116 1763059, 3~
      10 local_moran_pvalue standard     0.00317 (((381847 1762775, 381116 1763059, 3~
      # ... with 75 more rows

---

    Code
      (df_local_i_both <- ww_local_moran(guerry_modeled, crime_pers, predictions, ctg,
        wts))
    Output
      # A tibble: 170 x 4
         .metric       .estimator .estimate                                   geometry
         <chr>         <chr>          <dbl>                             <MULTIPOLYGON>
       1 local_moran_i standard      0.530  (((381847 1762775, 381116 1763059, 379972~
       2 local_moran_i standard      0.858  (((381847 1762775, 381116 1763059, 379972~
       3 local_moran_i standard      0.759  (((381847 1762775, 381116 1763059, 379972~
       4 local_moran_i standard      0.732  (((381847 1762775, 381116 1763059, 379972~
       5 local_moran_i standard      0.207  (((381847 1762775, 381116 1763059, 379972~
       6 local_moran_i standard      0.860  (((381847 1762775, 381116 1763059, 379972~
       7 local_moran_i standard      0.692  (((381847 1762775, 381116 1763059, 379972~
       8 local_moran_i standard      1.69   (((381847 1762775, 381116 1763059, 379972~
       9 local_moran_i standard     -0.0109 (((381847 1762775, 381116 1763059, 379972~
      10 local_moran_i standard      0.710  (((381847 1762775, 381116 1763059, 379972~
      # ... with 160 more rows

---

    Code
      (vec_local_i <- ww_local_moran_i_vec(guerry_modeled$crime_pers, guerry_modeled$
        predictions, ctg, wts))
    Output
       [1]  0.529586027  0.857962397  0.759397482  0.731821184  0.207216255
       [6]  0.859824645  0.692480894  1.685682868 -0.010937577  0.709971045
      [11]  1.756476080  0.839390997 -0.208812822  0.311287253 -0.195850256
      [16] -0.046485425  0.219659575  0.072248473  0.911260991  0.796818074
      [21]  0.472218810 -0.047995949 -0.701165391  0.682001844 -0.114131742
      [26]  0.043283334  1.067791069  1.186850176  0.174554949  0.071132504
      [31]  0.014932487  1.014614517  0.258635858  0.385988835 -0.113213840
      [36]  0.016531123  0.601974328 -0.029051514  0.101963855 -0.098393898
      [41]  0.305211136 -0.057462330 -0.015702560  0.882089292 -0.163892577
      [46]  1.649695545  0.377330987  0.868476489 -0.465975751  0.303084203
      [51]  1.404344537 -0.370062874  0.440556284  0.289554503  0.035787495
      [56]  0.393521099  1.006384006  0.222959827  0.730981130  0.628215009
      [61] -0.183012992  0.227295946  0.284153229  2.316505472  0.494418600
      [66]  0.982994320 -0.124397352  0.160297076  1.039537767  1.231583113
      [71]  0.271055716 -0.168894660 -0.038283576  0.017831736 -0.052920056
      [76]  1.205308932  0.808428811  0.551329387  0.878044848  0.901458850
      [81]  0.022009901 -0.327876773 -0.318368758 -0.003280457 -0.124796245

---

    Code
      (vec_local_i_p <- ww_local_moran_pvalue_vec(guerry_modeled$crime_pers,
      guerry_modeled$predictions, ctg, wts))
    Output
       [1] 0.194043674 0.010886137 0.012263744 0.059958742 0.119905829 0.046275338
       [7] 0.243193464 0.064112010 0.820873352 0.003173597 0.002068535 0.059995066
      [13] 0.879793574 0.001900848 0.754474453 0.727329506 0.012484788 0.370256366
      [19] 0.052134450 0.102170689 0.314809025 0.694682324 0.834171499 0.048195664
      [25] 0.643544752 0.297519485 0.130266426 0.001566132 0.015165249 0.201822930
      [31] 0.472123719 0.014869822 0.011885133 0.256350877 0.973892247 0.402810121
      [37] 0.080754741 0.568375225 0.067746216 0.577098572 0.089000231 0.862325548
      [43] 0.557549513 0.125467286 0.848939548 0.011991681 0.214002662 0.118936711
      [49] 0.982823060 0.202576766 0.002359295 0.771812517 0.068936309 0.092977267
      [55] 0.469066935 0.075684324 0.023316858 0.310572720 0.055652296 0.028159554
      [61] 0.847423723 0.192611624 0.337185557 0.025270426 0.199222009 0.189666001
      [67] 0.958603067 0.143820831 0.008989269 0.058385702 0.308984630 0.909502852
      [73] 0.642719638 0.500816936 0.692880319 0.079319750 0.022252122 0.037089571
      [79] 0.047283549 0.004620765 0.303598447 0.872677941 0.895620571 0.516574044
      [85] 0.842184818
