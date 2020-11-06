---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588417"
---
# <span data-ttu-id="cc837-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc837-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cc837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc837-102">SYNOPSIS</span></span>
<span data-ttu-id="cc837-103">PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="cc837-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc837-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc837-104">SYNTAX</span></span>

### <span data-ttu-id="cc837-105">Bykapaityorresourcegrouporsubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cc837-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc837-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="cc837-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc837-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc837-107">DESCRIPTION</span></span>
<span data-ttu-id="cc837-108">Get-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="cc837-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="cc837-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc837-109">EXAMPLES</span></span>

### <span data-ttu-id="cc837-110">Örnek 1: kaynak grubu kapasitelerini alma</span><span class="sxs-lookup"><span data-stu-id="cc837-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="cc837-111">Bu komut, testRG adlı kaynak grubundaki tüm Azure PowerBI eklenmiş kapasitesini alır</span><span class="sxs-lookup"><span data-stu-id="cc837-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="cc837-112">Örnek 2: kapasite edinme</span><span class="sxs-lookup"><span data-stu-id="cc837-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="cc837-113">Bu komut, testRG adlı kaynak grubundaki testcapacity adlı Azure PowerBI eklenmiş kapasitesini alır.</span><span class="sxs-lookup"><span data-stu-id="cc837-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="cc837-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc837-114">PARAMETERS</span></span>

### <span data-ttu-id="cc837-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc837-115">-DefaultProfile</span></span>
<span data-ttu-id="cc837-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc837-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc837-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc837-117">-Name</span></span>
<span data-ttu-id="cc837-118">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="cc837-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="cc837-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc837-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc837-120">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="cc837-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="cc837-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cc837-121">-ResourceId</span></span>
<span data-ttu-id="cc837-122">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="cc837-122">Azure resource ID</span></span>

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

### <span data-ttu-id="cc837-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc837-123">CommonParameters</span></span>
<span data-ttu-id="cc837-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc837-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc837-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc837-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc837-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc837-126">INPUTS</span></span>

### <span data-ttu-id="cc837-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cc837-127">System.String</span></span>

## <span data-ttu-id="cc837-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc837-128">OUTPUTS</span></span>

### <span data-ttu-id="cc837-129">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cc837-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cc837-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc837-130">NOTES</span></span>

## <span data-ttu-id="cc837-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc837-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc837-132">Yeni-Azurermpowerbibidedcapacity </span><span class="sxs-lookup"><span data-stu-id="cc837-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="cc837-133">Remove-Azurermpowerbibidedcapacity </span><span class="sxs-lookup"><span data-stu-id="cc837-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
