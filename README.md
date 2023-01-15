# Equity Futures Contract

The output of the model is the mark to market value of such a contract, that is, the Equity Futures price less the strike (if long position).

Let t be the current date, and let 0 be the trade date, T be the maturity date, Let   be the underlying (equity) price at time t,   be the Equity Futures price for maturity T, and K be the strike price (delivery price).

The payoff at time T of an Equity Futures contract (long position) is then  . 
The mark to market value of this contract at time t is:  .

Let   be the dates when corresponding discrete dollar dividends, , are paid (if a payment lag is applicable, then it should be added to the above dates). The present value of these dividends is then:

 ,

where   is the (continuously compounded) zero in interest rate applicable from t to T as seen at t,  is the distance between those dates in a given day count convention (usually, actual/365). Alternatively, let q be a (continuously compounded) dividend yield.

By no-arbitrage argument, the Equity Futures price is then: 

 .

Accordingly, the value of the Equity Futures contract (long position) at time t is: 

 

Delta, sensitivity to underlying, is going to be computed as follows:

 

In the following listings the symbol ”//” marks commented out text fragments containing either explanatory information or possible alternatives for the values of the corresponding attributes.

Deal 1

VALUATION_AS_OF_DATE                20050509
VALUATION_AS_OF_TIME                00:00

GREEKS DELTA

RANDOM_OBJECT_TYPE                  EQUITY
  UNDERLYING                        SPX
  EXCHANGE                          Z
  UND_CURRENCY                      USD=
  DRIFT_RATE_FILE                   USD_RATE_CURVE (see https://finpricing.com/lib/IrCurveIntroduction.html)
  DIVIDEND_FILE                     spx_div
  ASP                               1172.08                             
  STRIKE                            0

OPTION_TYPE                         EQUITY_FUTURES
  PAYOFF_CURRENCY                   USD=
  MODEL                             CLOSED_FORM
  CLASS                             EUROPEAN
  EXPDATE                           20050617
  EXPTIME                           17:00
  DISCOUNT_RATE_FILE                USD_RATE_CURVE

BEGIN_FILE_INFO         spx_div
SPX        Z   20050510        0.030443
SPX        Z   20050511        0.641146
SPX        Z   20050512        0.126079
SPX        Z   20050513        0.131578
SPX        Z   20050516        0.123795
SPX        Z   20050517        0.124188
SPX        Z   20050518        0.175363
SPX        Z   20050519        0.010361
SPX        Z   20050520        0.036185
SPX        Z   20050523        0.009276
SPX        Z   20050524        0.008820
SPX        Z   20050525        0.113729
SPX        Z   20050526        0.116603
SPX        Z   20050527        0.122092
SPX        Z   20050601        0.388127
SPX        Z   20050602        0.006363
SPX        Z   20050603        0.009627
SPX        Z   20050606        0.067421
SPX        Z   20050607        0.038778
SPX        Z   20050608        0.232640
SPX        Z   20050609        0.000359
SPX        Z   20050610        0.031369
SPX        Z   20050613        0.290447
SPX        Z   20050614        0.056587
SPX        Z   20050615        0.031406
SPX        Z   20050616        0.009151
SPX        Z   20050617        0.013423

