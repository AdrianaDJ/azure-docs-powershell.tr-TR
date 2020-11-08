---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106001"
---
# <span data-ttu-id="2c492-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="2c492-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="2c492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c492-102">SYNOPSIS</span></span>
<span data-ttu-id="2c492-103">Azure Media Services hesap anahtarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c492-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="2c492-104">**Not:** Bu sürüm kullanımdan kalktı, lütfen [daha yeni sürüme](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c492-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="2c492-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c492-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c492-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c492-106">DESCRIPTION</span></span>
<span data-ttu-id="2c492-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2c492-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2c492-108">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2c492-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2c492-109">**Yeni-Azuçözüm Aserviceskey** cmdlet 'ı belirtilen medya Hizmetleri hesabının birincil veya ikincil anahtarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c492-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="2c492-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c492-110">EXAMPLES</span></span>

### <span data-ttu-id="2c492-111">Örnek 1: Medya Hizmetleri hesap anahtarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2c492-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="2c492-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c492-112">PARAMETERS</span></span>

### <span data-ttu-id="2c492-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2c492-113">-Force</span></span>
<span data-ttu-id="2c492-114">Anahtar oluşturmanın onaylanmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c492-114">Indicates that the key generation is not confirmed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c492-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2c492-115">-KeyType</span></span>
<span data-ttu-id="2c492-116">Medya Hizmetleri anahtar türünü belirtir; Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2c492-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="2c492-117">Yararı</span><span class="sxs-lookup"><span data-stu-id="2c492-117">Primary</span></span>
- <span data-ttu-id="2c492-118">İK</span><span class="sxs-lookup"><span data-stu-id="2c492-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c492-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c492-119">-Name</span></span>
<span data-ttu-id="2c492-120">Medya Hizmetleri hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c492-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="2c492-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="2c492-121">-Profile</span></span>
<span data-ttu-id="2c492-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c492-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c492-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2c492-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c492-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c492-124">-Confirm</span></span>
<span data-ttu-id="2c492-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c492-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c492-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c492-126">-WhatIf</span></span>
<span data-ttu-id="2c492-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c492-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c492-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c492-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c492-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c492-129">CommonParameters</span></span>
<span data-ttu-id="2c492-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c492-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c492-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c492-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c492-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c492-132">INPUTS</span></span>

## <span data-ttu-id="2c492-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c492-133">OUTPUTS</span></span>

## <span data-ttu-id="2c492-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c492-134">NOTES</span></span>

## <span data-ttu-id="2c492-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c492-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c492-136">Medya Hizmetleri için Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="2c492-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


