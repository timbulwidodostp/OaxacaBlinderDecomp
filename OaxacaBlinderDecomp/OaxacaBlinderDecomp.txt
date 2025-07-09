# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Oaxaca-Blinder gap decomposition Use OaxacaBlinderDecomp (OaxacaBlinder) With (In) R Software
install.packages("remotes")
remotes::install_github("SinanPolatoglu/OaxacaBlinder")
library("OaxacaBlinder")
OaxacaBlinderDecomp = read.csv("https://raw.githubusercontent.com/timbulwidodostp/OaxacaBlinderDecomp/main/OaxacaBlinderDecomp/OaxacaBlinderDecomp.csv",sep = ";")
# Estimation Oaxaca-Blinder gap decomposition Use OaxacaBlinderDecomp (OaxacaBlinder) With (In) R Software
twofold = OaxacaBlinderDecomp(formula = real_wage ~ age + education | female, data = OaxacaBlinderDecomp, type = "twofold", baseline_invariant = TRUE, n_bootstraps = 100)
summary(twofold)
threefold = OaxacaBlinderDecomp(real_wage ~ age + education | female, OaxacaBlinderDecomp, type = "twofold", pooled = "jann", baseline_invariant = TRUE)
summary(threefold)
# Oaxaca-Blinder gap decomposition Use OaxacaBlinderDecomp (OaxacaBlinder) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished