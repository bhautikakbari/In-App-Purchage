## 📱 Store Configuration

<div style="background-color: #f6f8fa; padding: 20px; border-radius: 8px; margin: 20px 0;">
  <h3 style="color: #0366d6; margin-bottom: 20px;">Configuration Steps for Both Platforms</h3>
  
  <div style="display: flex; gap: 20px; flex-wrap: wrap;">
    <!-- iOS Configuration -->
    <div style="flex: 1; min-width: 300px; background-color: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      <h4 style="color: #1DA1F2; display: flex; align-items: center; gap: 8px;">
        <svg style="width: 24px; height: 24px;" viewBox="0 0 24 24" fill="currentColor">
          <path d="M17.05 20.28c-.98.95-2.05.8-3.08.35-1.09-.46-2.09-.48-3.24 0-1.44.62-2.2.44-3.06-.35C2.79 14.49 3.51 6.91 9.07 6.91c1.15-.03 2.24.74 2.93.75 1.11 0 2.13-.78 3.19-.75 1.83.06 3.14.96 3.94 2.42-3.28 1.72-2.76 6.2.92 7.42-.7 1.43-1.6 2.83-3 3.53zM12.03 6.4c-.09-2.87 2.35-5.2 5.19-5.4.26 2.81-2.24 5.31-5.19 5.4z"/>
        </svg>
        iOS Setup
      </h4>
      <div style="margin: 15px 0;">
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #1DA1F2;">1.</span>
          Open App Store Connect
        </p>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #1DA1F2;">2.</span>
          Navigate to Features > In-App Purchases
        </p>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #1DA1F2;">3.</span>
          Create subscription products with IDs:
        </p>
        <code style="display: block; background-color: #f6f8fa; padding: 10px; margin: 10px 0; border-radius: 4px;">
          ios_3months_sub
          ios_6months_sub
          ios_12months_sub
        </code>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #1DA1F2;">4.</span>
          Add to Info.plist:
        </p>
        <code style="display: block; background-color: #f6f8fa; padding: 10px; margin: 10px 0; border-radius: 4px;">
          &lt;key&gt;SKPaymentQueue&lt;/key&gt;
          &lt;true/&gt;
        </code>
      </div>
    </div>

    <!-- Android Configuration -->
    <div style="flex: 1; min-width: 300px; background-color: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      <h4 style="color: #3DDC84; display: flex; align-items: center; gap: 8px;">
        <svg style="width: 24px; height: 24px;" viewBox="0 0 24 24" fill="currentColor">
          <path d="M17.6 9.48l1.84-3.18c.16-.31.04-.69-.26-.85-.29-.15-.65-.06-.83.22l-1.88 3.24c-2.86-1.21-6.08-1.21-8.94 0L5.65 5.67c-.19-.29-.58-.38-.87-.2-.28.18-.37.54-.22.83L6.4 9.48C3.3 11.25 1.28 14.44 1 18h22c-.28-3.56-2.3-6.75-5.4-8.52zM7 15.25c-.69 0-1.25-.56-1.25-1.25s.56-1.25 1.25-1.25 1.25.56 1.25 1.25-.56 1.25-1.25 1.25zm10 0c-.69 0-1.25-.56-1.25-1.25s.56-1.25 1.25-1.25 1.25.56 1.25 1.25-.56 1.25-1.25 1.25z"/>
        </svg>
        Android Setup
      </h4>
      <div style="margin: 15px 0;">
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #3DDC84;">1.</span>
          Open Google Play Console
        </p>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #3DDC84;">2.</span>
          Navigate to Monetization setup
        </p>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #3DDC84;">3.</span>
          Create subscription products with IDs:
        </p>
        <code style="display: block; background-color: #f6f8fa; padding: 10px; margin: 10px 0; border-radius: 4px;">
          android_3months_sub
          android_6months_sub
          android_12months_sub
        </code>
        <p style="margin: 10px 0; padding-left: 20px; position: relative;">
          <span style="position: absolute; left: 0; color: #3DDC84;">4.</span>
          Add to AndroidManifest.xml:
        </p>
        <code style="display: block; background-color: #f6f8fa; padding: 10px; margin: 10px 0; border-radius: 4px;">
          &lt;uses-permission android:name="com.android.vending.BILLING" /&gt;
        </code>
      </div>
    </div>
  </div>

  <!-- Important Notes -->
  <div style="margin-top: 20px; padding: 15px; background-color: #fff3cd; border-left: 4px solid #ffc107; border-radius: 4px;">
    <h4 style="color: #856404; margin-bottom: 10px;">⚠️ Important Notes</h4>
    <ul style="list-style-type: none; padding-left: 0; margin: 0;">
      <li style="margin: 5px 0;">• iOS requires a paid Apple Developer account</li>
      <li style="margin: 5px 0;">• Android requires a one-time Play Console registration fee</li>
      <li style="margin: 5px 0;">• Test purchases using sandbox/test accounts before production</li>
      <li style="margin: 5px 0;">• Implement server-side receipt validation for security</li>
    </ul>
  </div>
</div>
