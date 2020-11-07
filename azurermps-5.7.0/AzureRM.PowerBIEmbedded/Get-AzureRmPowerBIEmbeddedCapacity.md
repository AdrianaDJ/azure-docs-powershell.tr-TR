---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762251"
---
# <span data-ttu-id="25156-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25156-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="25156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25156-102">SYNOPSIS</span></span>
<span data-ttu-id="25156-103">PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="25156-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25156-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="25156-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25156-105">DESCRIPTION</span></span>
<span data-ttu-id="25156-106">Get-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="25156-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="25156-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25156-107">EXAMPLES</span></span>

### <span data-ttu-id="25156-108">Örnek 1: kaynak grubu kapasitelerini alma</span><span class="sxs-lookup"><span data-stu-id="25156-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="25156-109">Bu komut, testRG adlı kaynak grubundaki tüm Azure PowerBI eklenmiş kapasitesini alır</span><span class="sxs-lookup"><span data-stu-id="25156-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="25156-110">Örnek 2: kapasite edinme</span><span class="sxs-lookup"><span data-stu-id="25156-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="25156-111">Bu komut, testRG adlı kaynak grubundaki testcapacity adlı Azure PowerBI eklenmiş kapasitesini alır.</span><span class="sxs-lookup"><span data-stu-id="25156-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="25156-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25156-112">PARAMETERS</span></span>

### <span data-ttu-id="25156-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25156-113">-ResourceGroupName</span></span>
<span data-ttu-id="25156-114">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="25156-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25156-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="25156-115">-Name</span></span>
<span data-ttu-id="25156-116">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="25156-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="25156-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="25156-117">-ResourceId</span></span>
<span data-ttu-id="25156-118">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="25156-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25156-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25156-119">CommonParameters</span></span>
<span data-ttu-id="25156-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25156-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25156-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25156-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25156-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25156-122">INPUTS</span></span>

### <span data-ttu-id="25156-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="25156-123">None</span></span>
<span data-ttu-id="25156-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="25156-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25156-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25156-125">OUTPUTS</span></span>

### <span data-ttu-id="25156-126">Liste<Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="25156-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="25156-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25156-127">NOTES</span></span>

## <span data-ttu-id="25156-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25156-128">RELATED LINKS</span></span>

[<span data-ttu-id="25156-129">Yeni-Azurermpowerbibidedcapacity </span><span class="sxs-lookup"><span data-stu-id="25156-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="25156-130">Remove-Azurermpowerbibidedcapacity </span><span class="sxs-lookup"><span data-stu-id="25156-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
