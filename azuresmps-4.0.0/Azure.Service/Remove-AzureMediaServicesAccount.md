---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106471"
---
# <span data-ttu-id="d9d9a-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d9d9a-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="d9d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d9a-103">Belirtilen Azure Media Services hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="d9d9a-104">**Not:**  Bu sürüm kullanımdan kalktı, lütfen [daha yeni sürüme](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="d9d9a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9d9a-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d9a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9d9a-106">DESCRIPTION</span></span>
<span data-ttu-id="d9d9a-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d9d9a-108">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d9d9a-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d9d9a-109">**Remove-Azuçözüm Aservicesaccount** cmdlet 'ı bir medya Hizmetleri hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="d9d9a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9d9a-110">EXAMPLES</span></span>

### <span data-ttu-id="d9d9a-111">Örnek 1: Medya Hizmetleri hesabını silme</span><span class="sxs-lookup"><span data-stu-id="d9d9a-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="d9d9a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9d9a-112">PARAMETERS</span></span>

### <span data-ttu-id="d9d9a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9d9a-113">-Force</span></span>
<span data-ttu-id="d9d9a-114">*Force* anahtarı belirtilmişse silme işlemi onaylanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="d9d9a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9d9a-115">-Name</span></span>
<span data-ttu-id="d9d9a-116">Medya Hizmetleri hesap adı.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="d9d9a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9d9a-117">-Profile</span></span>
<span data-ttu-id="d9d9a-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9d9a-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9d9a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9d9a-120">-Confirm</span></span>
<span data-ttu-id="d9d9a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d9a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d9a-122">-WhatIf</span></span>
<span data-ttu-id="d9d9a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9d9a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d9a-125">CommonParameters</span></span>
<span data-ttu-id="d9d9a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9d9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d9a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d9a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d9a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9d9a-128">INPUTS</span></span>

## <span data-ttu-id="d9d9a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9d9a-129">OUTPUTS</span></span>

## <span data-ttu-id="d9d9a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9d9a-130">NOTES</span></span>

## <span data-ttu-id="d9d9a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9d9a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9d9a-132">Medya Hizmetleri için Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="d9d9a-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="d9d9a-133">Get-Azuçözüm Aservicesaccount</span><span class="sxs-lookup"><span data-stu-id="d9d9a-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="d9d9a-134">Yeni-Azuçözüm Aservicesaccount</span><span class="sxs-lookup"><span data-stu-id="d9d9a-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


