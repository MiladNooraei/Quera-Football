# Football Analytics Project: From Transfermarkt Data Scraping to Predictive Insights

Welcome to the Football Analytics project! This repository showcases a comprehensive four-phase journey aimed at uncovering the hidden insights within football data. Through meticulous data scraping from the [Transfermarkt website](https://www.transfermarkt.com/) and subsequent analyses, we present a fresh perspective on the game we all love.

## Phases of the Project

### Phase 1: Data Collection
In the initial phase, we harnessed the power of Python's libraries, specifically Beautiful Soup 4 (BS4) and Selenium, to meticulously scrape valuable data from the top five European leagues: Spain, Germany, Italy, France, and England. The following dataset was collected:
```
Club Data
├── Big Five League from season 15/21
├── All Clubs
├── All players and their positions
├── All Rankings
├── All Squads
├── All total and average market values
├── All Ages and average ages
├── All Stadiums and their capacity
├── All coaches
├── All club victories and prizes
├── All club income | expenditure | OverallBalance
└── All foreign players
```
```
Players Data
├── Player Name
├── Player Full Name
├── Player ID
├── Player Shirt Number
├── Date of Birth
├── Citizenship
├── Place Of Birth
├── Caps
├── Goals
├── Other Positions
├── Foot
├── Outfitter
├── Agent
├── Contract Joined
├── Contract Expires
├── Date Of Last Contract
├── Height
├── Current Club
├── All Players Transfer Data (Season / Date / Market Value / Fee / Left / Joined)
├── All Players Stats
│   ├── Appearances
│   ├── Goals In Each Season
│   ├── Assists
│   ├── Yellow Card | Second Yellow Card | Red Card
│   ├── Minutes Played
│   └── Goals Conceded | Clean Sheets
└── ...

```

### Phase 2: Data Processing and Database Design

During this phase, we began by developing an [ER diagram](https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&layers=1&nav=1#R7V1bc5s4FP41mWkfnBF3eHSTtpvdpJekm15ePDLINi0BF8tNnF%2B%2FAgQGSTYYC9vxeqc7LUI3pE%2Bfzjk6Rz7TLh6e3sdwOrmJPBScqcB7OtMuz1RVtSyd%2FJWkLLIUxVSVLGUc%2Bx5NWybc%2Bc%2BIJgKaOvc9NKtkxFEUYH9aTXSjMEQurqTBOI4eq9lGUVBtdQrHiEu4c2HAp371PTzJUm3VWqb%2FhfzxJG9ZMZ3szQPMM9MvmU2gFz2WkrS3Z9pFHEU4%2B9fD0wUKktHLxyUr927F26JjMQpxkwJPdvD59xz%2B0u%2BvjA%2BzD4Zx9VPr0Vr%2BwGBOP%2Fgimoc4XtA%2B40U%2BELNH%2FyGAIXl64078wLuGi2ieNDzD0P2VP72ZRLH%2FHIUYBuSVQhLI6xjTeTVAJcddUpIkJ6kxadZDHi00Iu9pGUXPn2lfQFppHP0qJkRNyqMZyf8pHw1QJF3DGc67ks9A8taDs0naXvIAA38ckn%2B7pDSKk4TYpe0nzT9OfIzuptBNEh4J0pPPwA%2F5J478ILiIgihOR0ob2S5y3aKXpTdD29DTMeDnLp8IFGP0VEqic%2FkeRQ8onRZA3%2FY0jQKLLq2e6tCExyVQlTxtUgEpTYR0cYyL2pf4If%2BgENoATioHpzPVDDCdwXSZ5oNh%2Fp4nyCdDoQHyHxmwUpI5Tv6mUBxcXea1kE5lFWUZXl19%2BPI6fzeM2XIhfECv7vu3F3%2F1b0nbivGaQ3U%2B8QEaYW7GwiiFe3l6adKMYMEPx9dpqUudQWyCx2QifUIjfdoAjqY5JOGwwHEcYYhLzwQROVhL%2BOLRsnYt10OIIsZoiBezK7jkOCzTTzAfnrinNfcMFc8bAQ7J5I0CLM1BkrjHYahH0QRQskXUo3aGJX4r24p7CA5XE0%2FTmjWNr7lCWivqLXFZ0g%2BGyDQgID2Cdc%2BfP2R5%2FxAMTWD8yliX04UJi%2BFFkVsFr4%2BcIUFjpK%2BhSBGuLQmw9m%2F6gfdjfPPtGj%2FH08XztHd3X3S5NCPIIxIqfYxiPInGUQiDt8vUEqElQ7bMcx0lY5yO2E%2BE8YJOB5zjqDqe6MnH35Li5wZ9%2Bl56c%2FlEa04fFvRhwzmYRfPYRQ0WNOHwMVpbI82YjMvaOY1RALH%2FpyrZyyciXgi6Q3AWhadtrfW25gEXIVW0rRmmoViStjVGoBatfVOw9p3OtjRN6paWoXBjafo7IltD9uqYtwa1MVo2hIfeGTz0lUQDrsJRdOKb9io89BzPEPENRLqiqXL4RrVZMVqkwVsCTBXgkw8qoxPOIXDcmHiatDsaAZCM4qZctzsBfpuvWK%2BENBu25frPax9GsYfiHu1JP53s%2BFWvV05%2FnVVU9Gezfl8jOJ6jjXt%2BR9DobQGGVRPWJ0sSjtEgMfWu6NAoiCB%2B9VrQ8LsoJgsvHEwDuEDx7JUfYkGuvIkHGP9CuNCoFFVU5ReycQXNsl6FblTS58SZPpLGh5Awu1uX8%2B3TFIWej%2BdxXc5bGP5aORXHLAfojVl8jRwg5GzQGWdbHGdfRNCdnASAA7fhWxYjABR2hDp7Q3c6h916%2Fx%2BNRCZ8gsMWBvykFGP10sGRayBWY%2FhsaJzqTANReWGREg%2Fokf9P2ogkMhqNVDEZeebQNEw5ZGQAhow0fd8GENVsRUZ1SsGulZFmJHjE1FbwxMsxrqi8THXvu5hQDZqdqKw1lSHFM5AlojLHtDQoicoshTWsCKlM3yWVtZerRHaVDIubu0bk5RjZyjhy2UqVIluJANMdATnrCOgkX8m19lpQrOzppgF0OaSkM04TIpeJnUpXeQdeuHTVlAqPmd6cxmDcg3xlDxzv89z58f2pDz%2BTlflrMbAFjqfcDNX7ObBDX%2FZgCL1%2B4v5LHt%2FePsBwcca6RYh9HAq3BqGPA0r8CpNCPXAOUqJLU9KC5ypw8oRl6fSpUvwTin0yhglrrfCboGNT7yFBx6zeQ4LK37UeEmU4AAEcisTGrhS0jU%2BRn67s%2FKTdZLiQPc%2FKvp2WWkKNq0hnKuIOxrKx4SpKMVt8eHsYi07L9gVjqwWOFQbCRg2CtwCr1RCs6gmsHYFVZE3ZD1iVcwAqaD1X1PXeZcmDROY0XioYdZVRbW2miqZgtJmKOBdGeWAUS588dX6c45GPk%2Fk96TKtPeUgskdCXcZ0bTQcydFlehprYbFEFhZRMEF36kytsXgfrhCfUreBAen5CuVE7E9QLIX%2FWxCLJsVULAJed6qMSI9%2BSUIg0WUAIwhmPm671GVAwx05d9A4mB157%2BIhwQZclLJNkwyzNSKEUaVuxbCYNZDVKFX2FDir7m%2BRNA9q2IOilJ8U1K6E3H53WgmyFSWhE%2ByOwVqQ84bAK1SsinplrEX5FrTdWJFyTmDtRpHSeWbNhM7TMZFsNxxkrnDDsZwhkOUTyChWhcJfG9XfWWit3i4m4NAOiqgqttMmo5mP%2FRZBV7SvmY%2F4IB343GE7UQLV41YCC0qTrgTKiNMVC2N8rF7BwifGbWvMMpDt6SLGtdWhZkryFurpbByWkYs1tdcZOEZXeBLpS%2B39hVpy33siX4VCR2wuTGYeBGxGS5TxEmI0iEaDNz4RmlnDFucITtjzGYWziT%2Btu%2F%2BAfKGbVjxkKhZ3N4pwKY8pyJJd61SzKfApGQmuNzYGcDpDqb1xWcu7ZUVgmeUNRWDfBlNcsUIuoZknKsCq2ikJzCi9V%2FIBLtcUet76XFnfV2dgxmAYeQsuMRaOSr6c%2Bop%2BbjDfWFpqxUc6omZB%2Boe24zVqZ6uhbdyxVSgh8530k08U5hQNZ5KeQe1%2FEJVV7K7SYyMUXQKDi40ICjclL%2FvmjnwSao0C%2Bd5Vb8FqasuVfnOHeMbU%2FZt96PSl%2FkXqWdmEoxna2lkUnZCvMl92Z71sPKU7s%2FMwwp3GngM1tfP0OK9yjeWOrs2SvEvwzvHZ1h7extuuPQqVpgykHxxcuZBQ1qxzgHZJIVoLRewA0MoY0a3maCWaZoWFAVA3ZuEt2FR7qTju6SxbGlpLIKtMYKLGXl8q6VyUdFlhukyXzMotQTHZj9y4RH6Nq6zTVyE8DN43JjdNnuxTB2%2BfYi%2F6tQCv3BQXZu%2FmSMDgwyO3Mk%2B1tpPnBRnTk3rkAW3Fgt5GIRZiRoaF%2FO2j%2Fw5%2BjS1jcTf4Z%2Fj9eubOhwcU8VE9GlfXn42XvKRMRyvLEdUYkN24SRlNvegPRyCg%2BNPbnq%2BzArHW0FF50%2B2fkEa1IZNKX93uzHxc8JcYhrPRyQt6m2uwoWt7mmhjJvq%2FbniSNmaVCeksLtavC6tTOrtS3RDZCHZ%2BZp4c8tSd7SQbat2hzt9kiSKvLtfNfflsXNTWO7S870w1jvyW64JSpEeDSvnhCKFwcADeods63JUkiTYm900NrLUSQM4E%2B5cA8g3WqLKlzpJgY0usytgWuvKU7uka4yud%2FxbGyq6ZnP1u0xKKbXcvdpi8NE5EAXwyBhx85JXBGpBsAXmLXJ%2FUzn71x1QPQeboT6cIxsklqLOSOCCSBt5HMCjn0US1zfwZrsv0nQxO9DhwYeyVs6qiu22RG4XeYNG8xC3yGuW78cM5RrPsglqvlNla9ekD0hUXeZXMQu%2BbAMFwQNYLwuyQHrH4ZDZfkxs6H0qR%2Br0rPLgdOrc%2FPsx%2FfgWDsfpVAU1sK%2FsLnQHnpm1WhSoAau0mtdKeZMtKY7kqx8fhyFWMAGG1tbSwZ49mdyeGQhSLfu5iT0pAYttbSv4UtHotaFsbGFvhWDiITWF8OHGUOWzbHg8yqC0cPnaEWl51DdLr70%2BidHvzHUAaMkWiNEA2IPqRHFHaZpU7R%2BD2LbrKXcq5mhBMtZE2Xd5hsOp0LsPzmjsMWIFcUi9l3Lyb%2FRJo865Xvlj0u3vHIfmuZTLpP30g40xR2OMNbzQin%2B%2FjxW26T0Vh16bDhsICOHec6l1IOqiRGOTehcQLDOuoaf%2FyQuFKo7OmthcgQhhPk3%2BV8N9J3%2FvpXf2G9tXo7WfBzyZnNpCzU8zulpLEbmJ2ew4XtStytxAdqXDunW24UQiq2h8P7FqUEP0eyJReh5Siev%2FCxB5vhGpu3nypA6ClKOC7cDfxYzwI5w%2FDhOHEY1AK3%2BtuLC7gdNbtaGeW5k6b6I8Jb60Od5TaljuPE5YcuMF8yN4e31GTebhoQLaOxG6NY%2Bji1a4FnayVJiGddXXnG0GSR7GdKWaXEB90qBpKdZHtO56zm8HddtaK7TQd2jy4s%2FK1G4Zrrogg3b5LEkDQ8FMu6EoZ%2FGQ9aEoLposg1I5WjGo3GaxU%2BTytmGNdMe1AsOmKQU9Tn6gru1syx2FRWqvYbuWlLvREk2FSur%2Ftf1YnN8%2B%2F54ur9%2B67S%2B3p%2Bo%2FgKPWamvNBKs2dlPFtfsdulBrvOWVcMzVHk%2BSVqzDOYcWpe9kwZYgwJcNBRogp3r7DqGFtfl15U5v2Nk3SK7s2bVK8YF4owa1li61M5iIwynAV6d3HwSJ%2B%2BOD%2BHH9WlH%2FuPt0N7nqiwK0uD9m9j9nsJWwneiEpYnclcbw4uzbLX6rW8ob%2FnsI43PZYUElyk%2BV7XBcEu22BnuKozErYzkm2N%2Fj04%2BPtl1sQvfnm672%2F3zx%2Fvdx5xNqGSyU%2FPzrbwNlk5TIpHxOtY7qDWSY9zm26rddTtZ6GRz%2BN10jRPUvci2qzsvAslMYPIMhieU99BbXUH3DHtyocDpZtlt%2F0tmjmf5nDlI3ooiVDZ1sytgExeYyjROxcZicaxeQm8lCS4z8%3D) to guide the creation of a structured MySQL database. After meticulous data cleaning, we seamlessly utilized SQL Alchemy to establish the database, ensuring a robust foundation for our analysis.

### Phase 3: Statistical Analysis
In this phase, we leveraged statistical analysis to uncover insights and address pertinent questions related to the collected data. Below are some key inquiries we addressed:
- Player Participation Analysis in the 2021-2022 Season: Distribution of Match Appearances and Percentage of Involvement
- Exploring the Relationship Between Goals Scored and Estimated Player Value: A Linear Regression Analysis Using 2021-2022 Season Data
- Analyzing the Relationship Between Goals Scored and Estimated Market Value for Strikers in the 2021-2022 Season Using Linear Regression
- Exploring Estimated Player Prices Distribution by Position for the 2021-2022 Season Data
- Goal Scoring Analysis Across Different Leagues in the 2021-2022 Season
- Player Acquisition Costs Analysis across Seasons 2017-2018 to 2021-2022 in Football Leagues
- Discrepancy Between Player Transfer Fees and Actual Values in Football Industry: A Comparative Analysis
- Identifying Players with Performance in the Top 30% but Market Value in the Bottom 40%
- Comparing Performance Distribution of Players Obtained in the previous parts with the Overall Player Population
- Comparing Distribution of Players' Positions Obtained in the previous parts with the Overall Player Community
- Identifying Underperforming Players in Top 5 European Leagues Based on Performance Metrics
- Performance Comparison of Experienced and Young Football Players After Transfers to New Teams
- Performance Comparison of Teams in UEFA Champions League and Domestic Leagues

### Phase 4: Machine Learning Insights

In this pivotal phase, we harnessed the power of machine learning techniques to tackle three critical questions:

1. Predicting Player Market Value 
2. Player Post Classification
3. Player Similarity Clustering
## Authors

- [Farzaneh Soltanzadeh](https://github.com/FarzanehSoltanzadeh)
- [Milad Nooraei](https://github.com/MiladNooraei)
- [Zahra Honarvar](https://github.com/zahra-honarvar)
- [Ali Mousavi](https://github.com/Alimousavi48)
- [Mohammad Ghaffaripour](https://github.com/itsmohgh)
