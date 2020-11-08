---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098743"
---
# <span data-ttu-id="ae808-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae808-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="ae808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae808-102">SYNOPSIS</span></span>
<span data-ttu-id="ae808-103">Bir kaynak grubundaki veya abonelikteki sanal WAN veya tüm sanal WAN 'Lara sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ae808-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="ae808-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae808-104">SYNTAX</span></span>

### <span data-ttu-id="ae808-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae808-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae808-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae808-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae808-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae808-107">DESCRIPTION</span></span>
<span data-ttu-id="ae808-108">Bir kaynak grubundaki veya abonelikteki sanal WAN veya tüm sanal WAN 'Lara sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ae808-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="ae808-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae808-109">EXAMPLES</span></span>

### <span data-ttu-id="ae808-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae808-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ae808-111">Bu komut, testRG kaynak grubundaki myVirtualWAN adındaki sanal WAN 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="ae808-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="ae808-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ae808-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ae808-113">Bu komut "test" ile başlayan tüm sanal WAN 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="ae808-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="ae808-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae808-114">PARAMETERS</span></span>

### <span data-ttu-id="ae808-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae808-115">-DefaultProfile</span></span>
<span data-ttu-id="ae808-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae808-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae808-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae808-117">-Name</span></span>
<span data-ttu-id="ae808-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ae808-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ae808-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae808-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae808-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ae808-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ae808-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae808-121">CommonParameters</span></span>
<span data-ttu-id="ae808-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae808-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae808-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ae808-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae808-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae808-124">INPUTS</span></span>

### <span data-ttu-id="ae808-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ae808-125">None</span></span>

## <span data-ttu-id="ae808-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae808-126">OUTPUTS</span></span>

### <span data-ttu-id="ae808-127">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae808-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ae808-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae808-128">NOTES</span></span>

## <span data-ttu-id="ae808-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae808-129">RELATED LINKS</span></span>

[<span data-ttu-id="ae808-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae808-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="ae808-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae808-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="ae808-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae808-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
