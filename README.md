# Analysing stock prices of SPACs
Data Science Project for Open Uni: Identifying merging spacs for maximising profit in stock trading

### The Problem
Stock price prediction is a large field that has been researched for many years.

Although the field is broadly studied no single rule of thumb or bulletproof method exits for predicting stock prices

Since the stock market is driven by supply and demand many consider it to be unpredictable and prone to speculations.

Large investment companies trading on the stock market hire brokers and analysts who analyze prices using complex models including external information such as:  
- News feeds 
- Twitter activity
- Indicators of global market changes (https://www.federalreserve.gov/publications.htm)
- Company's profit Reports
- Industry specific and regulation changes  
- Black Swan events - unpredictable events that have a severe negative impact on the global economy

### Hypothesis
Our assumption is that by narrowing the research to a specific type of stocks (one having a similar behavior)
we could gain some certainty and produce a model that predicts prices
with high enough precision to make midterm buy/sell decisions.  
We chose to focus on SPAC stocks.

#### What is a SPAC?
SPAC is an acronym for a Special-Purpose Acquisition Company.
A company without clients, employees, staff or product.

It serves either of the 3 purposes bellow:
- Raise money through an Initial Public Offering (IPO)
- Find a private, target company
- Acquire or merge with the target company to provide them a means to enter the public equity market without the target company going through a traditional IPO themselves

Most Special-Purpose Acquisition Companies IPO with common shares offered at $10 a share. Once the deal is completed with the target company and the acquisition is successful, SPAC shareholders become shareholders of the acquired target company.

For the target companies, SPACs provide a means to access public equity markets without having to go through an expensive and tedious IPO process. They are also guaranteed the full fund raised by SPAC investors--hundreds of millions, if not billions of dollars--upon the merger, thus eliminating the concern of being unable to raise money from a lackluster IPO.
 
### Data Collection and Exploration
We Collected the data from yahoo finance and https://stockmarketmba.com/

The graphs include:
- Merge date (where available)
- Closing price
- Trading Volume

graphs were generated with plotly

#### list of SPAC symbols with their trading data collected from Yahoo Finance

[AADI](merged_spac_html/AADI.html)

[ACEL](merged_spac_html/ACEL.html)

[ACHR completed @ 2021-09-16](merged_spac_html/ACHR.html)

[ADN](merged_spac_html/ADN.html)

[ADSE completed @ 2021-12-23](merged_spac_html/ADSE.html)

[ADTH completed @ 2021-12-23](merged_spac_html/ADTH.html)

[ADV](merged_spac_html/ADV.html)

[AEVA completed @ 2021-03-12](merged_spac_html/AEVA.html)

[AGIL completed @ 2021-08-23](merged_spac_html/AGIL.html)

[AHCO](merged_spac_html/AHCO.html)

[ALIT](merged_spac_html/ALIT.html)

[ALLG](merged_spac_html/ALLG.html)

[AMBP](merged_spac_html/AMBP.html)

[AMPS completed @ 2021-12-09](merged_spac_html/AMPS.html)

[ANGH completed @ 2022-02-04](merged_spac_html/ANGH.html)

[APPH](merged_spac_html/APPH.html)

[ARBE](merged_spac_html/ARBE.html)

[ARKO](merged_spac_html/ARKO.html)

[ARQQ](merged_spac_html/ARQQ.html)

[ARVL](merged_spac_html/ARVL.html)

[ASLE](merged_spac_html/ASLE.html)

[ASTL](merged_spac_html/ASTL.html)

[ASTR completed @ 2021-06-30](merged_spac_html/ASTR.html)

[ASTS completed @ 2021-04-06](merged_spac_html/ASTS.html)

[ATIP completed @ 2021-06-16](merged_spac_html/ATIP.html)

[AUID](merged_spac_html/AUID.html)

[AUR completed @ 2021-11-03](merged_spac_html/AUR.html)

[AVPT completed @ 2021-07-01](merged_spac_html/AVPT.html)

[BARK completed @ 2021-06-01](merged_spac_html/BARK.html)

[BBAI completed @ 2021-12-07](merged_spac_html/BBAI.html)

[BBCP](merged_spac_html/BBCP.html)

[BFLY](merged_spac_html/BFLY.html)

[BGRY completed @ 2021-07-21](merged_spac_html/BGRY.html)

[BHIL completed @ 2021-09-29](merged_spac_html/BHIL.html)

[BKKT completed @ 2021-10-15](merged_spac_html/BKKT.html)

[BKSY completed @ 2021-09-09](merged_spac_html/BKSY.html)

[BLBX](merged_spac_html/BLBX.html)

[BLDE completed @ 2021-05-07](merged_spac_html/BLDE.html)

[BODY completed @ 2021-07-16](merged_spac_html/BODY.html)

[BOWL completed @ 2021-12-15](merged_spac_html/BOWL.html)

[BOXD completed @ 2021-12-08](merged_spac_html/BOXD.html)

[BTRS](merged_spac_html/BTRS.html)

[BTTX completed @ 2021-11-18](merged_spac_html/BTTX.html)

[BWMX](merged_spac_html/BWMX.html)

[BZFD completed @ 2021-12-03](merged_spac_html/BZFD.html)

[CANO completed @ 2021-06-03](merged_spac_html/CANO.html)

[CCCS completed @ 2021-07-30](merged_spac_html/CCCS.html)

[CDEV](merged_spac_html/CDEV.html)

[CELU completed @ 2021-07-16](merged_spac_html/CELU.html)

[CERE](merged_spac_html/CERE.html)

[CHPT completed @ 2021-03-09](merged_spac_html/CHPT.html)

[CIFR completed @ 2021-08-27](merged_spac_html/CIFR.html)

[CLBT](merged_spac_html/CLBT.html)

[CLNN](merged_spac_html/CLNN.html)

[CLOV](merged_spac_html/CLOV.html)

[CLVT](merged_spac_html/CLVT.html)

[CMAX completed @ 2021-06-08](merged_spac_html/CMAX.html)

[CMPO completed @ 2021-12-28](merged_spac_html/CMPO.html)

[CORZ completed @ 2022-02-07](merged_spac_html/CORZ.html)

[CPTN completed @ 2022-02-14](merged_spac_html/CPTN.html)

[CRXT completed @ 2021-09-09](merged_spac_html/CRXT.html)

[CTV completed @ 2021-11-30](merged_spac_html/CTV.html)

[CURI](merged_spac_html/CURI.html)

[CVT completed @ 2021-12-17](merged_spac_html/CVT.html)

[CYXT completed @ 2021-07-29](merged_spac_html/CYXT.html)

[CZOO](merged_spac_html/CZOO.html)

[DAVE completed @ 2022-01-05](merged_spac_html/DAVE.html)

[DCGO completed @ 2021-11-17](merged_spac_html/DCGO.html)

[DKNG](merged_spac_html/DKNG.html)

[DM](merged_spac_html/DM.html)

[DMTK](merged_spac_html/DMTK.html)

[DNA completed @ 2021-09-16](merged_spac_html/DNA.html)

[DNMR](merged_spac_html/DNMR.html)

[DOMA completed @ 2021-07-28](merged_spac_html/DOMA.html)

[DRTS completed @ 2022-03-08](merged_spac_html/DRTS.html)

[DSKE](merged_spac_html/DSKE.html)

[EFTR completed @ 2021-08-25](merged_spac_html/EFTR.html)

[ELMS completed @ 2021-06-25](merged_spac_html/ELMS.html)

[EMBK completed @ 2021-11-10](merged_spac_html/EMBK.html)

[ENJY completed @ 2021-10-15](merged_spac_html/ENJY.html)

[ENSC completed @ 2021-06-15](merged_spac_html/ENSC.html)

[ENVX completed @ 2021-07-14](merged_spac_html/ENVX.html)

[EOSE](merged_spac_html/EOSE.html)

[EQOS](merged_spac_html/EQOS.html)

[EQRX completed @ 2021-12-17](merged_spac_html/EQRX.html)

[ETWO](merged_spac_html/ETWO.html)

[EVEX completed @ 2022-05-09](merged_spac_html/EVEX.html)

[EVGO completed @ 2021-07-01](merged_spac_html/EVGO.html)

[EVLV completed @ 2021-07-16](merged_spac_html/EVLV.html)

[FATH completed @ 2021-12-23](merged_spac_html/FATH.html)

[FFIE completed @ 2021-07-21](merged_spac_html/FFIE.html)

[FREE](merged_spac_html/FREE.html)

[FREY](merged_spac_html/FREY.html)

[FRGE completed @ 2022-03-21](merged_spac_html/FRGE.html)

[FSR](merged_spac_html/FSR.html)

[FSRD completed @ 2022-02-04](merged_spac_html/FSRD.html)

[GB](merged_spac_html/GB.html)

[GCMG](merged_spac_html/GCMG.html)

[GDYN](merged_spac_html/GDYN.html)

[GENI](merged_spac_html/GENI.html)

[GGR](merged_spac_html/GGR.html)

[GLS completed @ 2022-01-13](merged_spac_html/GLS.html)

[GMTX](merged_spac_html/GMTX.html)

[GOEV](merged_spac_html/GOEV.html)

[GRAB](merged_spac_html/GRAB.html)

[GRNA completed @ 2022-02-02](merged_spac_html/GRNA.html)

[GWH completed @ 2021-10-08](merged_spac_html/GWH.html)

[HFFG](merged_spac_html/HFFG.html)

[HGTY completed @ 2021-12-02](merged_spac_html/HGTY.html)

[HIMS](merged_spac_html/HIMS.html)

[HIPO completed @ 2021-08-02](merged_spac_html/HIPO.html)

[HLBZ completed @ 2021-09-10](merged_spac_html/HLBZ.html)

[HLGN completed @ 2021-12-30](merged_spac_html/HLGN.html)

[HLLY completed @ 2021-07-16](merged_spac_html/HLLY.html)

[HLMN completed @ 2021-07-14](merged_spac_html/HLMN.html)

[HUMA completed @ 2021-08-26](merged_spac_html/HUMA.html)

[HYLN](merged_spac_html/HYLN.html)

[HYMC](merged_spac_html/HYMC.html)

[HYPR completed @ 2021-12-22](merged_spac_html/HYPR.html)

[HYZN completed @ 2021-07-16](merged_spac_html/HYZN.html)

[ID](merged_spac_html/ID.html)

[IMTX](merged_spac_html/IMTX.html)

[IMVT](merged_spac_html/IMVT.html)

[IMXI](merged_spac_html/IMXI.html)

[INDI](merged_spac_html/INDI.html)

[INVZ](merged_spac_html/INVZ.html)

[IONQ completed @ 2021-09-30](merged_spac_html/IONQ.html)

[IRNT completed @ 2021-08-26](merged_spac_html/IRNT.html)

[IS](merged_spac_html/IS.html)

[ISPO completed @ 2022-02-14](merged_spac_html/ISPO.html)

[ISUN](merged_spac_html/ISUN.html)

[JBI](merged_spac_html/JBI.html)

[JOBY completed @ 2021-08-10](merged_spac_html/JOBY.html)

[JSPR completed @ 2021-09-24](merged_spac_html/JSPR.html)

[KERN](merged_spac_html/KERN.html)

[KIND completed @ 2021-11-18](merged_spac_html/KIND.html)

[KLR](merged_spac_html/KLR.html)

[KORE](merged_spac_html/KORE.html)

[KPLT completed @ 2021-06-09](merged_spac_html/KPLT.html)

[KXIN](merged_spac_html/KXIN.html)

[LAZR](merged_spac_html/LAZR.html)

[LCID completed @ 2021-07-23](merged_spac_html/LCID.html)

[LEV](merged_spac_html/LEV.html)

[LFG completed @ 2021-09-15](merged_spac_html/LFG.html)

[LFLY completed @ 2022-02-04](merged_spac_html/LFLY.html)

[LLAP completed @ 2022-03-25](merged_spac_html/LLAP.html)

[LOCL completed @ 2021-11-19](merged_spac_html/LOCL.html)

[LOTZ](merged_spac_html/LOTZ.html)

[LPRO](merged_spac_html/LPRO.html)

[LSEA](merged_spac_html/LSEA.html)

[LTCH completed @ 2021-06-04](merged_spac_html/LTCH.html)

[LTRY completed @ 2021-11-19](merged_spac_html/LTRY.html)

[LVOX completed @ 2021-06-21](merged_spac_html/LVOX.html)

[MAPS completed @ 2021-06-15](merged_spac_html/MAPS.html)

[ME completed @ 2021-06-16](merged_spac_html/ME.html)

[MGY](merged_spac_html/MGY.html)

[MILE](merged_spac_html/MILE.html)

[MIMO completed @ 2021-08-13](merged_spac_html/MIMO.html)

[MIR completed @ 2021-10-20](merged_spac_html/MIR.html)

[MKFG completed @ 2021-07-14](merged_spac_html/MKFG.html)

[MKTW completed @ 2021-07-21](merged_spac_html/MKTW.html)

[ML](merged_spac_html/ML.html)

[MLTX completed @ 2022-04-05](merged_spac_html/MLTX.html)

[MNTS completed @ 2021-08-12](merged_spac_html/MNTS.html)

[MP](merged_spac_html/MP.html)

[MPLN](merged_spac_html/MPLN.html)

[MTTR completed @ 2021-07-22](merged_spac_html/MTTR.html)

[MULN](merged_spac_html/MULN.html)

[MVST completed @ 2021-07-23](merged_spac_html/MVST.html)

[MYPS completed @ 2021-06-21](merged_spac_html/MYPS.html)

[NAUT completed @ 2021-06-09](merged_spac_html/NAUT.html)

[NKLA](merged_spac_html/NKLA.html)

[NN](merged_spac_html/NN.html)

[NRDY completed @ 2021-09-20](merged_spac_html/NRDY.html)

[NRGV completed @ 2022-02-14](merged_spac_html/NRGV.html)

[NRXP completed @ 2021-05-24](merged_spac_html/NRXP.html)

[NUVB](merged_spac_html/NUVB.html)

[NVTS completed @ 2021-10-19](merged_spac_html/NVTS.html)

[NVVE](merged_spac_html/NVVE.html)

[OPAD completed @ 2021-09-01](merged_spac_html/OPAD.html)

[OPEN completed @ 2020-12-18](merged_spac_html/OPEN.html)

[OPFI completed @ 2021-07-20](merged_spac_html/OPFI.html)

[ORGN completed @ 2021-06-24](merged_spac_html/ORGN.html)

[OSW](merged_spac_html/OSW.html)

[OTMO](merged_spac_html/OTMO.html)

[OUST completed @ 2021-03-11](merged_spac_html/OUST.html)

[OWL completed @ 2021-05-19](merged_spac_html/OWL.html)

[OWLT completed @ 2021-07-15](merged_spac_html/OWLT.html)

[PACK](merged_spac_html/PACK.html)

[PAYA](merged_spac_html/PAYA.html)

[PAYO](merged_spac_html/PAYO.html)

[PCT](merged_spac_html/PCT.html)

[PEAR completed @ 2021-12-03](merged_spac_html/PEAR.html)

[PHUN](merged_spac_html/PHUN.html)

[PIII completed @ 2021-12-03](merged_spac_html/PIII.html)

[PL completed @ 2021-12-07](merged_spac_html/PL.html)

[PLBY](merged_spac_html/PLBY.html)

[PNT completed @ 2021-06-30](merged_spac_html/PNT.html)

[PRCH](merged_spac_html/PRCH.html)

[PRDS completed @ 2021-12-23](merged_spac_html/PRDS.html)

[PRPL](merged_spac_html/PRPL.html)

[PSFE](merged_spac_html/PSFE.html)

[PTRA completed @ 2021-06-14](merged_spac_html/PTRA.html)

[PWP completed @ 2021-06-24](merged_spac_html/PWP.html)

[QNGY completed @ 2022-02-08](merged_spac_html/QNGY.html)

[QS](merged_spac_html/QS.html)

[QSI completed @ 2021-06-15](merged_spac_html/QSI.html)

[QTEK completed @ 2022-02-25](merged_spac_html/QTEK.html)

[RBOT completed @ 2021-09-17](merged_spac_html/RBOT.html)

[RCOR completed @ 2021-09-02](merged_spac_html/RCOR.html)

[RDBX completed @ 2021-10-22](merged_spac_html/RDBX.html)

[RDW completed @ 2021-09-02](merged_spac_html/RDW.html)

[REE](merged_spac_html/REE.html)

[REVB completed @ 2022-01-11](merged_spac_html/REVB.html)

[RGTI completed @ 2022-03-01](merged_spac_html/RGTI.html)

[RIDE](merged_spac_html/RIDE.html)

[RKLB completed @ 2021-08-24](merged_spac_html/RKLB.html)

[RMO](merged_spac_html/RMO.html)

[ROIV](merged_spac_html/ROIV.html)

[ROVR completed @ 2021-07-30](merged_spac_html/ROVR.html)

[RPAY](merged_spac_html/RPAY.html)

[RSI](merged_spac_html/RSI.html)

[RSVR completed @ 2021-07-28](merged_spac_html/RSVR.html)

[SABS completed @ 2021-10-22](merged_spac_html/SABS.html)

[SAI completed @ 2022-05-02](merged_spac_html/SAI.html)

[SATL completed @ 2022-01-26](merged_spac_html/SATL.html)

[SEAT](merged_spac_html/SEAT.html)

[SES completed @ 2022-02-03](merged_spac_html/SES.html)

[SFT](merged_spac_html/SFT.html)

[SGHC](merged_spac_html/SGHC.html)

[SHCR completed @ 2021-07-01](merged_spac_html/SHCR.html)

[SHPW completed @ 2021-09-29](merged_spac_html/SHPW.html)

[SKIL completed @ 2021-06-15](merged_spac_html/SKIL.html)

[SKIN completed @ 2021-05-05](merged_spac_html/SKIN.html)

[SKLZ](merged_spac_html/SKLZ.html)

[SKYH completed @ 2022-02-07](merged_spac_html/SKYH.html)

[SLDP completed @ 2021-12-08](merged_spac_html/SLDP.html)

[SLGC completed @ 2021-09-01](merged_spac_html/SLGC.html)

[SMFR completed @ 2021-07-22](merged_spac_html/SMFR.html)

[SMPL](merged_spac_html/SMPL.html)

[SMR completed @ 2022-05-02](merged_spac_html/SMR.html)

[SMRT completed @ 2021-08-24](merged_spac_html/SMRT.html)

[SNAX completed @ 2021-07-20](merged_spac_html/SNAX.html)

[SNCE completed @ 2021-10-06](merged_spac_html/SNCE.html)

[SOFI completed @ 2021-05-28](merged_spac_html/SOFI.html)

[SOND completed @ 2022-01-18](merged_spac_html/SOND.html)

[SOUN completed @ 2022-04-27](merged_spac_html/SOUN.html)

[SPCE](merged_spac_html/SPCE.html)

[SPIR completed @ 2021-08-16](merged_spac_html/SPIR.html)

[SRZN completed @ 2021-08-11](merged_spac_html/SRZN.html)

[SST completed @ 2022-02-07](merged_spac_html/SST.html)

[STEM completed @ 2021-04-28](merged_spac_html/STEM.html)

[STRC completed @ 2021-09-24](merged_spac_html/STRC.html)

[STRY](merged_spac_html/STRY.html)

[SUNL completed @ 2021-07-09](merged_spac_html/SUNL.html)

[SWVL](merged_spac_html/SWVL.html)

[TALK completed @ 2021-07-16](merged_spac_html/TALK.html)

[TMC completed @ 2021-09-09](merged_spac_html/TMC.html)

[TNGX completed @ 2021-08-10](merged_spac_html/TNGX.html)

[TOI completed @ 2021-11-12](merged_spac_html/TOI.html)

[TTCF](merged_spac_html/TTCF.html)

[UK](merged_spac_html/UK.html)

[UP completed @ 2021-07-13](merged_spac_html/UP.html)

[UPH completed @ 2021-06-09](merged_spac_html/UPH.html)

[USWS](merged_spac_html/USWS.html)

[UTZ](merged_spac_html/UTZ.html)

[UWMC](merged_spac_html/UWMC.html)

[VCSA completed @ 2021-12-06](merged_spac_html/VCSA.html)

[VIEW](merged_spac_html/VIEW.html)

[VINC](merged_spac_html/VINC.html)

[VLD completed @ 2021-09-29](merged_spac_html/VLD.html)

[VLDR](merged_spac_html/VLDR.html)

[VLTA completed @ 2021-08-26](merged_spac_html/VLTA.html)

[VORB completed @ 2021-12-31](merged_spac_html/VORB.html)

[VRRM](merged_spac_html/VRRM.html)

[VRT](merged_spac_html/VRT.html)

[VVNT](merged_spac_html/VVNT.html)

[VWE completed @ 2021-06-07](merged_spac_html/VWE.html)

[WE completed @ 2021-10-20](merged_spac_html/WE.html)

[WEJO](merged_spac_html/WEJO.html)

[WSC](merged_spac_html/WSC.html)

[XELA](merged_spac_html/XELA.html)

[XL](merged_spac_html/XL.html)

[XOS completed @ 2021-08-19](merged_spac_html/XOS.html)

[YTRA](merged_spac_html/YTRA.html)

[ZEV completed @ 2021-05-06](merged_spac_html/ZEV.html)

#### conclusions
Most of the merged companies were traded around 10$ persistently until some time around the merge.
The trading volume is also persistently low before the acquisition.

[data collection notebook](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/ds_project_data_collection.ipynb)

### Experiments and Anlysis
We started by trying to predict the price of a single stock based on a 30 day observation.
In several attempts we tried to use different subsets of features and different outputs (predict the closing price only vs all of the input features as well)
We also tried several techniques for predicting multiple time steps ahead (predicting 4 days at a time vs predicting 1 day and feeding it back to the model in a loop)

At first we tried to predict a single stock closing price using only a sequence of closing prices from 60 days before</br>
[Experiment 1](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/single_stock_prediction_with_lstm.ipynb)

We then tried using multiple generated features in various combinations, trying to predict several days ahead, training the model on all using different stocks data</br>
[Experiment 2](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/predicting_4d_base_on_25d_input.ipynb)

[Experiment 3](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/prediction_with_nasdaq_feature.ipynb)

We attempted to compare the prediction results with GRU vs LSTM</br> 
[Experiment 4](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/ds_project_gru_vs_lstm.ipynb)

At last we tried to predict several time steps ahead by back feeding the output of the model as input</br>
[Experiment 5](https://colab.research.google.com/github/vladgrish/ds_spac_project/blob/gh-pages/using_model_prediction_as_input.ipynb)

*** TODO: add notebooks and description

#### Notice: 
As we realized many of the examples over the internet don't really predict multiple days ahead but rather use new incoming data up to one day before predicted day and only plot the prediction to look like a multi step forcast (hence the lag seen in graphs)

We understood that such results are not usable in real life as it does not allow to make a decision several days ahead. 
Our last attempt of predicting 20 days ahead gave interesting results. 
- the predicted price was never above the actual price
- the predicted timespan had an increase or decrease in price in the first few steps followed by a plateau
- although the price range around the peak was different for every stock,
using minmax normalization we were able to use a single model for multiple stocks
- It appears that when predicting multiple time steps the prediction resembles line more than it does a sawtooth or curve this could be a linked with either the activation function of the last layer, the cost funtion used or the inconsistent variance in the input data, however we did not manage to overcome it (yet)

### Conclusions and Next Steps
Conclusions:
- While predicting one day ahead at a time results can be pretty accurate it's not really usable
- Making midterm predictions several days ahead is magnitude harder
- Feeding the output of the model as input amplifies biases and creates distortions in the data that may seem random

For our next steps we would like to:
- Fine-tune the model configuration and achieve better understanding of the limitations of our NN with each configuration
- Address the prediction as indicator of a trend rather than the actual price
- Better Validate the results for false positives
- Create a simple function that can be run daily against a premerged SPAC stock list, the uses the trained model and returning a Buy\Don't Buy decision for each stock with the expected price and revenue  

### Terminology
- ticker symbol - the 3-4 letter string by which a company is identified in the stock market
- open price - the price of the stock at the beginning of day 
- close price - the end of day price 
- volume - the total amount of money the stock was traded that day
- high - stocks daily highest selling price
- low - stocks daily lowest selling price
