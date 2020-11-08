---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105785"
---
# <span data-ttu-id="53bee-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="53bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bee-102">SYNOPSIS</span></span>
<span data-ttu-id="53bee-103">Belirtilen Web sitesinde tarayıcıyı açar.</span><span class="sxs-lookup"><span data-stu-id="53bee-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="53bee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53bee-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53bee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="53bee-105">DESCRIPTION</span></span>
<span data-ttu-id="53bee-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="53bee-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="53bee-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="53bee-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="53bee-108">**Show-AzureWebsite** cmdlet 'i belirtilen Web sitesinde bir tarayıcı açar.</span><span class="sxs-lookup"><span data-stu-id="53bee-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="53bee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53bee-109">EXAMPLES</span></span>

## <span data-ttu-id="53bee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53bee-110">PARAMETERS</span></span>

### <span data-ttu-id="53bee-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="53bee-111">-Name</span></span>
<span data-ttu-id="53bee-112">Tarayıcıda açılacak sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bee-112">Specifies the name of the site to open in the browser.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bee-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="53bee-113">-Profile</span></span>
<span data-ttu-id="53bee-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bee-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53bee-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="53bee-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53bee-116">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="53bee-116">-Slot</span></span>
<span data-ttu-id="53bee-117">Web sitesinin yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53bee-117">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bee-118">CommonParameters</span></span>
<span data-ttu-id="53bee-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53bee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bee-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bee-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53bee-121">INPUTS</span></span>

## <span data-ttu-id="53bee-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53bee-122">OUTPUTS</span></span>

## <span data-ttu-id="53bee-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53bee-123">NOTES</span></span>

## <span data-ttu-id="53bee-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53bee-124">RELATED LINKS</span></span>

[<span data-ttu-id="53bee-125">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="53bee-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="53bee-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="53bee-127">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="53bee-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="53bee-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="53bee-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53bee-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


