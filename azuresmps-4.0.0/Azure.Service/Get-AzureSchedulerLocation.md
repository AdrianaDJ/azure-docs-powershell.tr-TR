---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105611"
---
# <span data-ttu-id="a2326-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="a2326-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="a2326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2326-102">SYNOPSIS</span></span>
<span data-ttu-id="a2326-103">Kullanılabilir Planlayıcı konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2326-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="a2326-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2326-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2326-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2326-105">DESCRIPTION</span></span>
<span data-ttu-id="a2326-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a2326-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a2326-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a2326-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a2326-108">**Get-AzureSchedulerLocation** cmdlet 'i kullanılabilir Zamanlayıcı konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2326-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="a2326-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2326-109">EXAMPLES</span></span>

### <span data-ttu-id="a2326-110">Örnek 1: kullanılabilir Planlayıcı konumlarını alma</span><span class="sxs-lookup"><span data-stu-id="a2326-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="a2326-111">Bu komut kullanılabilir Zamanlayıcı konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2326-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="a2326-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2326-112">PARAMETERS</span></span>

### <span data-ttu-id="a2326-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2326-113">-Profile</span></span>
<span data-ttu-id="a2326-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2326-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2326-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a2326-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2326-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2326-116">CommonParameters</span></span>
<span data-ttu-id="a2326-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2326-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2326-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2326-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2326-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2326-119">INPUTS</span></span>

## <span data-ttu-id="a2326-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2326-120">OUTPUTS</span></span>

## <span data-ttu-id="a2326-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2326-121">NOTES</span></span>

## <span data-ttu-id="a2326-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2326-122">RELATED LINKS</span></span>

[<span data-ttu-id="a2326-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a2326-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="a2326-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a2326-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a2326-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="a2326-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


