---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273569"
---
# <span data-ttu-id="c970b-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="c970b-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="c970b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c970b-102">SYNOPSIS</span></span>
<span data-ttu-id="c970b-103">Verilen işletim sistemi ve plan türü için bir işlev uygulamasının kullanılabildiği konumu alır.</span><span class="sxs-lookup"><span data-stu-id="c970b-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="c970b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c970b-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c970b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c970b-105">DESCRIPTION</span></span>
<span data-ttu-id="c970b-106">Verilen işletim sistemi ve plan türü için bir işlev uygulamasının kullanılabildiği konumu alır.</span><span class="sxs-lookup"><span data-stu-id="c970b-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="c970b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c970b-107">EXAMPLES</span></span>

### <span data-ttu-id="c970b-108">Örnek 1: Windows için Premium 'un uygun olduğu konumları edinin.</span><span class="sxs-lookup"><span data-stu-id="c970b-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="c970b-109">Parametre belirtilmemişse, Plantürü ' Premium ' olarak ve OSType ' Windows ' olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c970b-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="c970b-110">Bu komut, Windows için Premium 'un uygun olduğu konumları alır.</span><span class="sxs-lookup"><span data-stu-id="c970b-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="c970b-111">Örnek 2: burada, Linux 'un ekstra olduğu konumları edinin.</span><span class="sxs-lookup"><span data-stu-id="c970b-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="c970b-112">Bu komut, Linux için Premium 'un kullanılabileceği konumları alır.</span><span class="sxs-lookup"><span data-stu-id="c970b-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="c970b-113">Örnek 3: Windows için tüketimin kullanılabildiği konumları edinin.</span><span class="sxs-lookup"><span data-stu-id="c970b-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="c970b-114">Bu komut, Windows için tüketimin kullanılabileceği konumları alır.</span><span class="sxs-lookup"><span data-stu-id="c970b-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="c970b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c970b-115">PARAMETERS</span></span>

### <span data-ttu-id="c970b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c970b-116">-DefaultProfile</span></span>
<span data-ttu-id="c970b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c970b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970b-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="c970b-118">-OSType</span></span>
<span data-ttu-id="c970b-119">Hizmet planının işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="c970b-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970b-120">-Plantürü</span><span class="sxs-lookup"><span data-stu-id="c970b-120">-PlanType</span></span>
<span data-ttu-id="c970b-121">Plan türü.</span><span class="sxs-lookup"><span data-stu-id="c970b-121">The plan type.</span></span>
<span data-ttu-id="c970b-122">Geçerli girişler: tüketim veya Premium</span><span class="sxs-lookup"><span data-stu-id="c970b-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970b-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c970b-123">-SubscriptionId</span></span>
<span data-ttu-id="c970b-124">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c970b-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c970b-125">CommonParameters</span></span>
<span data-ttu-id="c970b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c970b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c970b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c970b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c970b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c970b-128">INPUTS</span></span>

## <span data-ttu-id="c970b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c970b-129">OUTPUTS</span></span>

### <span data-ttu-id="c970b-130">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıgeoregion</span><span class="sxs-lookup"><span data-stu-id="c970b-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="c970b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c970b-131">NOTES</span></span>

<span data-ttu-id="c970b-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c970b-132">ALIASES</span></span>

## <span data-ttu-id="c970b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c970b-133">RELATED LINKS</span></span>

