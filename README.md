import React from "react";

// README-style React component that displays project information + dashboard image.
// USAGE:
// 1. Put your dashboard image file (exported from the Excel workbook) into the public/ folder
//    and name it `dashboard.png` (or update the <img> src below).
// 2. Import and render <ReadmeWithDashboard /> inside your app (e.g. in App.jsx).

export default function ReadmeWithDashboard() {
  return (
    <div className="min-h-screen bg-gray-50 p-6">
      <div className="max-w-4xl mx-auto bg-white rounded-2xl shadow-lg p-8">
        <header className="mb-6">
          <h1 className="text-3xl font-semibold mb-2">Sales Performance Pattern Analysis</h1>
          <p className="text-sm text-gray-600">README + embedded dashboard image — generated from your Excel workbook.</p>
        </header>

        <section className="mb-6">
          <h2 className="text-xl font-medium mb-2">Overview</h2>
          <p className="text-gray-700">This project analyzes year-over-year sales performance using Excel pivot tables and charts. The component below shows the dashboard screenshot so viewers can quickly see the visuals used in the analysis.</p>
        </section>

        <section className="mb-6">
          <h2 className="text-xl font-medium mb-2">Dashboard</h2>
          <div className="border rounded-xl overflow-hidden shadow-sm">
            {/* Replace the src with the correct path if your image filename is different */}
            <img src="/dashboard.png" alt="Sales Dashboard Screenshot" className="w-full h-auto object-contain" />
          </div>
          <p className="text-xs text-gray-500 mt-2">Tip: export the dashboard from Excel as PNG and place it at <code>public/dashboard.png</code>.</p>
        </section>

        <section className="mb-6">
          <h2 className="text-xl font-medium mb-2">Key Stats (from GRAND TOTAL)</h2>
          <ul className="list-disc list-inside text-gray-700">
            <li><strong>2021:</strong> 1,094,539 boxes — ₹18,631,494 (or currency as in source)</li>
            <li><strong>2022:</strong> 250,035 boxes — ₹3,070,228</li>
            <li><strong>Grand Total:</strong> 1,344,574 boxes — ₹21,701,722</li>
          </ul>
        </section>

        <section className="mb-6">
          <h2 className="text-xl font-medium mb-2">How to reproduce</h2>
          <ol className="list-decimal list-inside text-gray-700">
            <li>Open the Excel workbook: <code>SALES PERFORMANCE PATTERN ANALYSIS DASHBOARD USING EXCEL.xlsx</code>.</li>
            <li>Navigate to the <em>DASHBOARD</em> sheet and take a screenshot or export as PNG.</li>
            <li>Place the PNG into your React app's <code>public/</code> folder named <code>dashboard.png</code>.</li>
            <li>Start your React app and the image will display inside this README component.</li>
          </ol>
        </section>

        <section>
          <h2 className="text-lg font-medium mb-2">Want changes?</h2>
          <p className="text-gray-700">I can also:
            <ul className="list-disc list-inside">
              <li>Generate a Markdown README with embedded image links instead of React.</li>
              <li>Export the dashboard image from the Excel file for you (if you upload it or allow export).</li>
              <li>Convert this to a single-file static HTML page.</li>
            </ul>
          </p>
        </section>
      </div>
    </div>
  );
}
