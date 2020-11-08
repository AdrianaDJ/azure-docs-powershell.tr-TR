---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106272"
---
# <span data-ttu-id="b7284-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="b7284-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="b7284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7284-102">SYNOPSIS</span></span>
<span data-ttu-id="b7284-103">Kullanılabilir tüm Web sitesi konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b7284-103">Gets all available website locations.</span></span>

## <span data-ttu-id="b7284-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7284-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7284-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7284-105">DESCRIPTION</span></span>
<span data-ttu-id="b7284-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b7284-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b7284-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b7284-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b7284-108">Geçerli aboneliğin kullanılabilir tüm Web sitesi konumlarını alır</span><span class="sxs-lookup"><span data-stu-id="b7284-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="b7284-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7284-109">EXAMPLES</span></span>

### <span data-ttu-id="b7284-110">Örnek 1: tüm kullanılabilir konumları al</span><span class="sxs-lookup"><span data-stu-id="b7284-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="b7284-111">Bu örnekte, geçerli aboneliğin kullanılabilir tüm Web sitesi konumları alınır.</span><span class="sxs-lookup"><span data-stu-id="b7284-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="b7284-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7284-112">PARAMETERS</span></span>

### <span data-ttu-id="b7284-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="b7284-113">-Profile</span></span>
<span data-ttu-id="b7284-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7284-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7284-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b7284-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7284-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7284-116">CommonParameters</span></span>
<span data-ttu-id="b7284-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7284-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7284-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7284-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7284-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7284-119">INPUTS</span></span>

## <span data-ttu-id="b7284-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7284-120">OUTPUTS</span></span>

## <span data-ttu-id="b7284-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7284-121">NOTES</span></span>

## <span data-ttu-id="b7284-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7284-122">RELATED LINKS</span></span>

[<span data-ttu-id="b7284-123">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b7284-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


