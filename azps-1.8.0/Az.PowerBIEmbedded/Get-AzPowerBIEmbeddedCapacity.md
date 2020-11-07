---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759819"
---
# <span data-ttu-id="b9534-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b9534-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b9534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9534-102">SYNOPSIS</span></span>
<span data-ttu-id="b9534-103">PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b9534-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b9534-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9534-104">SYNTAX</span></span>

### <span data-ttu-id="b9534-105">Bykapaityorresourcegrouporsubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9534-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9534-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b9534-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9534-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9534-107">DESCRIPTION</span></span>
<span data-ttu-id="b9534-108">Get-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b9534-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b9534-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9534-109">EXAMPLES</span></span>

### <span data-ttu-id="b9534-110">Örnek 1: kaynak grubu kapasitelerini alma</span><span class="sxs-lookup"><span data-stu-id="b9534-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="b9534-111">Bu komut, testRG adlı kaynak grubundaki tüm Azure PowerBI eklenmiş kapasitesini alır</span><span class="sxs-lookup"><span data-stu-id="b9534-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="b9534-112">Örnek 2: kapasite edinme</span><span class="sxs-lookup"><span data-stu-id="b9534-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="b9534-113">Bu komut, testRG adlı kaynak grubundaki testcapacity adlı Azure PowerBI eklenmiş kapasitesini alır.</span><span class="sxs-lookup"><span data-stu-id="b9534-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="b9534-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9534-114">PARAMETERS</span></span>

### <span data-ttu-id="b9534-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9534-115">-DefaultProfile</span></span>
<span data-ttu-id="b9534-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9534-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9534-117">-Name</span></span>
<span data-ttu-id="b9534-118">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="b9534-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9534-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9534-120">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b9534-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b9534-121">-ResourceId</span></span>
<span data-ttu-id="b9534-122">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="b9534-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9534-123">CommonParameters</span></span>
<span data-ttu-id="b9534-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9534-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9534-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9534-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9534-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9534-126">INPUTS</span></span>

### <span data-ttu-id="b9534-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9534-127">System.String</span></span>

## <span data-ttu-id="b9534-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9534-128">OUTPUTS</span></span>

### <span data-ttu-id="b9534-129">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b9534-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b9534-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9534-130">NOTES</span></span>

## <span data-ttu-id="b9534-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9534-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9534-132">Yeni-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="b9534-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b9534-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="b9534-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
