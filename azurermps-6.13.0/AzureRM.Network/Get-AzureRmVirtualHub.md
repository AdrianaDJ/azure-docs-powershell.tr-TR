---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764939"
---
# <span data-ttu-id="01d99-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="01d99-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="01d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d99-102">SYNOPSIS</span></span>
<span data-ttu-id="01d99-103">Bir Azure VirtualHub 'ı Name ve ResourceGroupName ile alır veya tüm sanal hubları ResourceGroupName/Subscription ile listeler.</span><span class="sxs-lookup"><span data-stu-id="01d99-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01d99-104">SYNTAX</span></span>

### <span data-ttu-id="01d99-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01d99-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01d99-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d99-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01d99-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01d99-107">DESCRIPTION</span></span>
<span data-ttu-id="01d99-108">Bir Azure VirtualHub 'ı Name ve ResourceGroupName ile alır veya tüm sanal hubları ResourceGroupName/Subscription ile listeler.</span><span class="sxs-lookup"><span data-stu-id="01d99-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="01d99-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01d99-109">EXAMPLES</span></span>

### <span data-ttu-id="01d99-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01d99-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="01d99-111">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="01d99-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="01d99-112">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="01d99-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="01d99-113">Ardından, sanal hub 'ı, ResourceGroupName ve ResourceName kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="01d99-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="01d99-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01d99-114">PARAMETERS</span></span>

### <span data-ttu-id="01d99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d99-115">-DefaultProfile</span></span>
<span data-ttu-id="01d99-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01d99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d99-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="01d99-117">-Name</span></span>
<span data-ttu-id="01d99-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="01d99-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d99-119">-ResourceGroupName</span></span>
<span data-ttu-id="01d99-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01d99-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d99-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d99-121">CommonParameters</span></span>
<span data-ttu-id="01d99-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01d99-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d99-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d99-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d99-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01d99-124">INPUTS</span></span>

### <span data-ttu-id="01d99-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="01d99-125">None</span></span>

## <span data-ttu-id="01d99-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01d99-126">OUTPUTS</span></span>

### <span data-ttu-id="01d99-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="01d99-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="01d99-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01d99-128">NOTES</span></span>

## <span data-ttu-id="01d99-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01d99-129">RELATED LINKS</span></span>
