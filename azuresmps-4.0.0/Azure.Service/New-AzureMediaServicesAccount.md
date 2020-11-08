---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105911"
---
# <span data-ttu-id="35393-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="35393-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="35393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35393-102">SYNOPSIS</span></span>
<span data-ttu-id="35393-103">Azure Media Services hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35393-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="35393-104">**Not:** Bu sürüm kullanımdan kalktı, lütfen [daha yeni sürüme](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)bakın.</span><span class="sxs-lookup"><span data-stu-id="35393-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="35393-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35393-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35393-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="35393-106">DESCRIPTION</span></span>
<span data-ttu-id="35393-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="35393-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="35393-108">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="35393-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="35393-109">**New-Azuçözüm Aservicesaccount** cmdlet 'i, belirtilen medya Hizmetleri hesap adı, SAP, hesap oluşturmak istediğiniz ve var olan bir depolama hesabı adı içeren yeni bir medya Hizmetleri hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35393-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="35393-110">Depolama hesabının yeni medya Hizmetleri hesabıyla aynı veri merkezinde bulunması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="35393-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="35393-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35393-111">EXAMPLES</span></span>

### <span data-ttu-id="35393-112">Örnek 1: yeni bir medya Hizmetleri hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="35393-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="35393-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35393-113">PARAMETERS</span></span>

### <span data-ttu-id="35393-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="35393-114">-Location</span></span>
<span data-ttu-id="35393-115">Media Services Datacenter konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="35393-115">Specifies the Media Services datacenter location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35393-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="35393-116">-Name</span></span>
<span data-ttu-id="35393-117">Medya Hizmetleri hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35393-117">Specifies the Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35393-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="35393-118">-Profile</span></span>
<span data-ttu-id="35393-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35393-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35393-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="35393-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35393-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35393-121">-StorageAccountName</span></span>
<span data-ttu-id="35393-122">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35393-122">Specifies the storage account name.</span></span>
<span data-ttu-id="35393-123">Depolama hesabının yeni medya Hizmetleri hesabıyla aynı veri merkezinde varolması gerekir.</span><span class="sxs-lookup"><span data-stu-id="35393-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35393-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35393-124">CommonParameters</span></span>
<span data-ttu-id="35393-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35393-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35393-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35393-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35393-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35393-127">INPUTS</span></span>

## <span data-ttu-id="35393-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35393-128">OUTPUTS</span></span>

## <span data-ttu-id="35393-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35393-129">NOTES</span></span>

## <span data-ttu-id="35393-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35393-130">RELATED LINKS</span></span>

[<span data-ttu-id="35393-131">Medya Hizmetleri için Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="35393-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="35393-132">Get-Azuçözüm Aservicesaccount</span><span class="sxs-lookup"><span data-stu-id="35393-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="35393-133">Remove-Azuçözüm Aservicesaccount</span><span class="sxs-lookup"><span data-stu-id="35393-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


