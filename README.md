# 🇦🇹 Austria Self-Employment Tax Calculator 2025

A lightweight, single-file HTML/JS calculator designed to estimate Net Income, Income Tax, and Social Security (SVS) contributions for freelancers and self-employed individuals in Austria. 

Targeted for the **2025 tax year**, this tool handles complex Austrian specificities like the *Kleinunternehmer* flat rates, profit allowances (*Gewinnfreibetrag*), and social security thresholds.

![License](https://img.shields.io/badge/license-MIT-green)
![Language](https://img.shields.io/badge/languages-DE%20%7C%20EN%20%7C%20SL%20%7C%20UA-blue)
![Platform](https://img.shields.io/badge/platform-Web-orange)

## 🌟 Features

*   **Zero Dependencies:** A single `index.html` file. No build process, no backend, runs offline.
*   **2025 Tax Rules:** Updated for projected 2025 tax brackets and SVS contribution limits.
*   **Smart Expense Logic:**
    *   **Kleinunternehmer-Pauschalierung:** Supports 20% (Service/Knowledge) and 45% (Trade/Production).
    *   **Basispauschalierung:** Supports 6% and 12% for higher earners (up to 220k).
*   **Employment Modes:**
    *   **Hauptberuflich (Full-Time):** Calculates full SVS (Pension, Health, Self-employment).
    *   **Nebenberuflich (Side Business):** Handles the *Geringfügig* threshold (~6,221€) where only accident insurance applies.
*   **Family & Tax Credits:**
    *   **Familienbonus Plus:** Direct tax reduction per child.
    *   **Sole Earner (AVAB):** Refundable tax credit logic included.
*   **Profit Allowance (GFB):** Automatically calculates the tax-free *Grundfreibetrag* (15% up to 30k profit).
*   **Multi-Language Support:** Auto-detects browser language. Fully translated into **German, English, Slovenian, and Ukrainian**.
*   **UX/UI:** Dark mode support, responsive design, and helpful tooltips explaining Austrian tax laws.

## 🚀 How to Use
*   Run at `https://ankhezar.github.io/at.tax.calculator/`.

## 🧠 Tax Logic Implemented

This calculator is strictly based on Austrian Tax Law (*EStG*) and Social Security Law (*GSVG*).

### 1. Expenses (Pauschalierung)
Users can choose between two flat-rate expense models:
*   **Small Business (Kleinunternehmer):**
    *   **Service:** 20% expenses (Revenue < 40k/55k).
    *   **Trade:** 45% expenses (Revenue < 40k/55k).
    *   *Includes warnings for the "Once every 5 years" tolerance rule.*
*   **Basic Flat Rate (Basispauschalierung):**
    *   **Service:** 6% expenses.
    *   **Trade:** 12% expenses.

### 2. Social Security (SVS)
*   **Full-Time:** Uses ~26% rate (Health 6.8%, Pension 18.5%, Self-empl 1.53%) + Accident insurance.
*   **Side Business:** Checks if profit is below the marginal earnings threshold (~6,221€). If below, calculates only accident insurance (~136€/year). If above, calculates full contribution.

### 3. Income Tax (Einkommensteuer)
*   Calculates **Tax Base**: `Revenue - Flat Expenses - Paid SVS - Profit Allowance (15%)`.
*   Applies the progressive Austrian tax brackets (0%, 20%, 30%, 40%, 48%, 50%).
*   Deducts **Tax Credits** (Family Bonus, AVAB) from the calculated tax.

## ⚠️ Disclaimer

**This tool is for informational purposes only.** 
While every effort has been made to ensure accuracy based on 2025 projections, this calculator does not constitute financial or legal advice. 
*   It does not replace a tax advisor (*Steuerberater*).
*   SVS contributions are often provisional and subject to recalculation (*Nachzahlung*) in the third year.
*   The "Profit Allowance" is calculated based on the automatic basic allowance (*Grundfreibetrag*).

## 📄 License

This project is licensed under the MIT License - feel free to use, modify, and distribute.
