# WalletInc.Model.WalletConfiguration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HeaderBackgroundColor** | **string** |  | 
**HeaderButtonColor** | **string** |  | 
**LeftMenuHeaderBackgroundColor** | **string** |  | 
**LeftMenuHeaderFontColor** | **string** |  | 
**LeftMenuSectionBackgroundColor** | **string** |  | 
**LeftMenuSectionFontColor** | **string** |  | 
**CompanyLogoURL** | **string** |  | 
**HeaderImageURL** | **string** |  | [optional] 
**HeaderCustomIcon** | **string** |  | [optional] 
**WelcomeMessage** | **string** |  | 
**IsAppleEnabled** | **bool** |  | 
**IsGoogleEnabled** | **bool** |  | 
**IsSamsungEnabled** | **bool** |  | 
**IsAdCredits** | **bool** |  | 
**IsStaticVouchers** | **bool** |  | 
**IsDynamicVouchers** | **bool** |  | 
**IsMembershipTier** | **bool** |  | 
**IsMembershipPoints** | **bool** |  | 
**IsMembershipLevel** | **bool** |  | 
**IsGiftCards** | **bool** |  | 
**IsGiftCertificates** | **bool** |  | 
**IsPromotions** | **bool** |  | 
**IsMerchantCredit** | **bool** |  | 
**IsTickets** | **bool** |  | [optional] 
**IsNewsArticles** | **bool** |  | 
**IsPerformances** | **bool** |  | 
**IsMessages** | **bool** |  | 
**IsCall** | **bool** |  | 
**IsRepresentatives** | **bool** |  | 
**IsProducts** | **bool** |  | 
**IsServices** | **bool** |  | 
**IsRoomRates** | **bool** |  | 
**IsAmenities** | **bool** |  | 
**IsGaming** | **bool** |  | 
**IsDining** | **bool** |  | 
**IsLounges** | **bool** |  | 
**IsMapDirections** | **bool** |  | 
**IsLinkBook** | **bool** |  | 
**IsImageGrid** | **bool** |  | 
**IsVideos** | **bool** |  | 
**IsTransactionHistory** | **bool** |  | 
**IsProfile** | **bool** |  | 
**IsSettings** | **bool** |  | 
**IsChatRoom** | **bool** |  | 
**IsSmsOptIn** | **bool** |  | 
**SmsOptInSourceID** | [**WTWalletConfigurationSaveWalletRecordSmsOptInSourceID**](WTWalletConfigurationSaveWalletRecordSmsOptInSourceID.md) |  | [optional] 
**IsEmailSubscriber** | **bool** |  | 
**GoogleAnalyticsID** | **string** |  | [optional] 
**FacebookPixelID** | **string** |  | [optional] 
**PublicChatRoomChannelID** | **double** |  | [optional] 
**VanityHandle** | **string** |  | [optional] 
**VanityPageWalletPrefix** | **string** |  | [optional] 
**MerchantCreditPaymentDesignID** | **string** |  | [optional] 
**CustomDomain** | **string** |  | [optional] 
**IsClaimed** | **bool** |  | [optional] 
**MobileAppIconURL** | **string** |  | [optional] 
**IsAgeGate** | **bool** |  | [optional] 
**IsFlipRequiredForQR** | **bool** |  | [optional] 
**AgeGateMinimum** | **double** |  | [optional] 
**AgeGateDeclineURL** | **string** |  | [optional] 
**SocialInstagramURL** | **string** |  | [optional] 
**SocialFacebookURL** | **string** |  | [optional] 
**SocialYouTubeURL** | **string** |  | [optional] 
**SocialTwitterURL** | **string** |  | [optional] 
**SocialLinkedInURL** | **string** |  | [optional] 
**SocialBackgroundColor** | **string** |  | [optional] 
**SocialFontColor** | **string** |  | [optional] 
**PrimaryPhoneNumber** | **string** |  | [optional] 
**PrimaryWhatsApp** | **string** |  | [optional] 
**PrimaryEmailAddress** | **string** |  | [optional] 
**CustomJS** | **string** |  | [optional] 
**CustomCSS** | **string** |  | [optional] 
**NonMobileRedirectURL** | **string** |  | [optional] 
**AppleAppStoreURL** | **string** |  | [optional] 
**GooglePlayStoreURL** | **string** |  | [optional] 
**PassBrandKit** | [**WTPassBrandKit**](WTPassBrandKit.md) |  | [optional] 
**Id** | **string** |  | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**MerchantID** | **string** |  | 
**AndroidSHA256Fingerprint** | **string** | SHA-256 fingerprint of the merchant&#39;s Android signing certificate, in Android&#39;s colon-separated uppercase hex format (e.g. \&quot;A1:B2:C3:...\&quot;). Populated by the POST /v2/wallet/android/keystore endpoint and consumed by the assetlinks.json endpoint so Google can verify the merchant&#39;s TWA ownership. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

