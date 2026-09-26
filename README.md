# Sovereignty Simulator

When could you stop working and live on what you own, with bitcoin? This simulator finds your **freedom year**:
the first year you could stop earning, with what you own paying for your life through 2050. The answer stands in
cast metal on wet ground at dawn; the sooner it comes, the higher the sun.

## A fork of Bitcoin24

This repository is a fork of [Bitcoin24](https://github.com/bitcoin-model/bitcoin_model) by Michael Saylor,
Shirish Jajodia and Chaitanya Jain. It keeps Bitcoin24's history and files as its base: `Bitcoin24 v1.0.xlsm`,
`bitcoin.png`, and Bitcoin24's README (below), at commit 30c97a7.

- **From Bitcoin24:** the bear, base and bull price cases, the macro model of world assets, the asset returns and
  the five strategies (Normie, BTC 10%, BTC Maxi, Double Maxi, Triple Maxi), re-implemented in JavaScript.
  Comments in `js/model.js` cite the workbook cells they come from.
- **Added here, not in Bitcoin24:**
  - the freedom-year search and the years after it, when you stop earning and live on what you own. While you
    work, your pay covers your costs; any gap comes out of your savings, then out of what you own;
  - after 2045, where Bitcoin24 stops, bitcoin grows with the world's other assets, and your inflation and
    bitcoin's yearly growth ease toward 2% (the gap halves every 5 years);
  - the plan ends in 2050: past that, too much will change for the numbers to mean much;
  - capital gains tax on the bitcoin you sell, from your cost basis and your rate;
  - borrowing against your bitcoin instead of selling it: interest, a borrowing cap, and the lender's liquidation
    level;
  - swapping part of your bitcoin for STRC, Strategy's variable-rate preferred stock: its dividend rate and its
    return-of-capital tax treatment (sources linked on the page);
  - bitcoin maturing: loan rates and STRC's dividend fall in a straight line to the mortgage rate by 2050;
  - a four-year cycle: bitcoin rises above its path, then falls a chosen share of its price the next year, each
    fall 15% smaller than the last, so you can see what crashes do to a loan;
  - warnings: numbers in a risky zone turn red, with the reason listed under the results.

This project is not affiliated with Bitcoin24's authors or with Strategy. An illustration, not financial or tax
advice.

## Run it

No build step. Serve the folder and open it in a browser:

```
python3 -m http.server 8000        # then open http://localhost:8000
```

Test the model (Node 18 or later, no packages needed):

```
node tools/test-sim.mjs
```

The tests check the model against the Bitcoin24 workbook's figures, against hand-worked tax, loan, STRC and
cycle cases, and against the simulator's first version (`reference/v2.html`).

## Files

- `index.html`, `css/sim.css`: the page.
- `js/model.js`: the model, with no page code.
- `js/ui.js`: the controls, results, chart, warnings and year-by-year table.
- `js/scene.js`: the sunrise scene, drawn with three.js. The years use Playfair Display's lining figures
  (`data/sim-glyphs.json`).
- `vendor/three/`: three.js (MIT licence), only the files the scene uses.
- `fonts/`: Cormorant Garamond, Figtree, JetBrains Mono and Playfair Display (SIL Open Font License).

## Licence

The files this fork adds are under the MIT licence (`LICENSE`). Bitcoin24's own files (`Bitcoin24 v1.0.xlsm`,
`bitcoin.png` and the README text below) come from github.com/bitcoin-model/bitcoin_model, which states no licence;
they keep their authors' terms.

---

## Bitcoin24's README

## Bitcoin24 <img src="https://github.com/bitcoin-model/bitcoin_model/blob/main/bitcoin.png" width="30" height="30">
Helping you drive Bitcoin adoption.

### 21-year macro forecast with micro models for bitcoin strategies
<table style="background-color: orange;">
  <tr>
    <th>Normie</th>
    <th>BTC 10%</th>
    <th>BTC Maxi</th>
    <th>Double Maxi</th>
    <th>Triple Maxi</th>
  </tr>
</table>

Bitcoin24 is designed to simulate 21-year outcomes of various Bitcoin strategies tailored for individuals, corporations, institutions, and nation-states. Users can input their own assumptions or adjust the model to explore different scenarios. Saving the file will automatically update the scenario comparison charts in the micro models' bottom section.

Bitcoin24 does not model Bitcoin's volatility, as its volatility profile has evolved and will continue to do so in the future. This is a simplified model intended to show possible long-term outcomes of adopting a Bitcoin standard.
<table>
  <tr>
    <th>21-Year Forecasting</th>
    <th>Flexible Assumptions</th>
  </tr>
</table>

#### Original Contributors
- <a href= "https://x.com/saylor">Michael J. Saylor</a>
- <a href="https://x.com/shirishjajodia">Shirish Jajodia</a>
- <a href="https://x.com/_ChaitanyaJ">Chaitanya Jain (CJ)</a>

<br>
<br>

>"It might make sense just to get some in case it catches on. If enough people think the same way, that becomes a self-fulfilling prophecy." - Satoshi Nakamoto on 01/17/09 (BTC Price: $0)

<br>
<br>

> [!TIP]
> 1. <a href="https://github.com/user-attachments/assets/2710d05e-cfce-41a9-84ec-eb39d0afc6e0">Bitcoin24 - Intro</a>
> 2. <a href="https://github.com/user-attachments/assets/d6842ec0-f919-4f82-8ee2-10bcc3fe8f97">Bitcoin24 - BTC</a>
> 3. <a href="https://github.com/user-attachments/assets/1379c00b-7b38-435a-8ec3-b43fd3319871">Bitcoin24 - Macro</a>
> 4. <a href="https://github.com/user-attachments/assets/3ce97819-e76e-449f-ab4a-3405dcc098f5">Bitcoin24 - Individual</a>
> 5. <a href="https://github.com/user-attachments/assets/8afa6ed9-301d-4c3d-8f90-ad1556043155">Bitcoin24 - Corporate</a>
> 6. <a href="https://github.com/user-attachments/assets/eaffca98-cb3f-4ec3-bec8-4d44b6b6fe1f">Bitcoin24 - Institution</a>
> 7. <a href="https://github.com/user-attachments/assets/6cc536b6-9087-4231-993b-b1a42477b2ae">Bitcoin24 - Nation State</a>
> 8. <a href="https://github.com/user-attachments/assets/37aab46f-a840-4aed-a48d-8179f1b48d50">Bitcoin24 - United States</a>
<br>
<br>
<br>





>Additional Information:  The information provided here is for general informational purposes only and should not be considered financial advice. It contains forward-looking information that is inherently unknowable. You should seek advice from a professional financial advisor and other trusted sources before acting on any of this information. The authors and publishers of this information disclaim responsibility for any action taken by users of this information.  This is but one view of potential outcomes. You should inform yourself of other views, including those that might disagree.





