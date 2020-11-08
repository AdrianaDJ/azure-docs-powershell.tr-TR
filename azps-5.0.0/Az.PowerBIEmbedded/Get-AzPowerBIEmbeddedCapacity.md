---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278495"
---
# <span data-ttu-id="fc611-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc611-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc611-102">SYNOPSIS</span></span>
<span data-ttu-id="fc611-103">PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fc611-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fc611-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc611-104">SYNTAX</span></span>

### <span data-ttu-id="fc611-105">Bykapaityorresourcegrouporsubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc611-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc611-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fc611-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc611-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc611-107">DESCRIPTION</span></span>
<span data-ttu-id="fc611-108">Get-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fc611-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fc611-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc611-109">EXAMPLES</span></span>

### <span data-ttu-id="fc611-110">Örnek 1: kaynak grubu kapasitelerini alma</span><span class="sxs-lookup"><span data-stu-id="fc611-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="fc611-111">Bu komut, testRG adlı kaynak grubundaki tüm Azure PowerBI eklenmiş kapasitesini alır</span><span class="sxs-lookup"><span data-stu-id="fc611-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="fc611-112">Örnek 2: kapasite edinme</span><span class="sxs-lookup"><span data-stu-id="fc611-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="fc611-113">Bu komut, testRG adlı kaynak grubundaki testcapacity adlı Azure PowerBI eklenmiş kapasitesini alır.</span><span class="sxs-lookup"><span data-stu-id="fc611-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="fc611-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc611-114">PARAMETERS</span></span>

### <span data-ttu-id="fc611-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc611-115">-DefaultProfile</span></span>
<span data-ttu-id="fc611-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc611-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc611-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc611-117">-Name</span></span>
<span data-ttu-id="fc611-118">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="fc611-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="fc611-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc611-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc611-120">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="fc611-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="fc611-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc611-121">-ResourceId</span></span>
<span data-ttu-id="fc611-122">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="fc611-122">Azure resource ID</span></span>

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

### <span data-ttu-id="fc611-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc611-123">CommonParameters</span></span>
<span data-ttu-id="fc611-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc611-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc611-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc611-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc611-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc611-126">INPUTS</span></span>

### <span data-ttu-id="fc611-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fc611-127">System.String</span></span>

## <span data-ttu-id="fc611-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc611-128">OUTPUTS</span></span>

### <span data-ttu-id="fc611-129">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc611-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc611-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc611-130">NOTES</span></span>

## <span data-ttu-id="fc611-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc611-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc611-132">Yeni-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="fc611-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fc611-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="fc611-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
