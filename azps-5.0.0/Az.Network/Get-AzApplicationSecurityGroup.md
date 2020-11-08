---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279970"
---
# <span data-ttu-id="cff1d-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cff1d-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="cff1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff1d-102">SYNOPSIS</span></span>
<span data-ttu-id="cff1d-103">Uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="cff1d-103">Gets an application security group.</span></span>

## <span data-ttu-id="cff1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cff1d-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cff1d-105">DESCRIPTION</span></span>
<span data-ttu-id="cff1d-106">**Get-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="cff1d-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="cff1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cff1d-107">EXAMPLES</span></span>

### <span data-ttu-id="cff1d-108">Örnek 1: tüm uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="cff1d-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="cff1d-109">Yukarıdaki komut, abonelikteki tüm uygulama güvenlik gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cff1d-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="cff1d-110">Örnek 2: kaynak grubundaki uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="cff1d-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="cff1d-111">Yukarıdaki komut MyResourceGroup kaynak grubuna ait tüm uygulama güvenlik gruplarını getirir.</span><span class="sxs-lookup"><span data-stu-id="cff1d-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cff1d-112">Örnek 3: belirli bir uygulama güvenlik grubunu alma.</span><span class="sxs-lookup"><span data-stu-id="cff1d-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="cff1d-113">Yukarıdaki komut MyApplicationSecurityGroup kaynak grubunun altındaki uygulama güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="cff1d-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cff1d-114">Örnek 4: filtreleme kullanarak uygulama güvenlik gruplarını alma.</span><span class="sxs-lookup"><span data-stu-id="cff1d-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="cff1d-115">Yukarıdaki komut, "MyApplicationSecurityGroup" ile başlayan tüm uygulama güvenlik gruplarını getirir.</span><span class="sxs-lookup"><span data-stu-id="cff1d-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="cff1d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cff1d-116">PARAMETERS</span></span>

### <span data-ttu-id="cff1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff1d-117">-DefaultProfile</span></span>
<span data-ttu-id="cff1d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cff1d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cff1d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="cff1d-119">-Name</span></span>
<span data-ttu-id="cff1d-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cff1d-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cff1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="cff1d-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cff1d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cff1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff1d-123">CommonParameters</span></span>
<span data-ttu-id="cff1d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cff1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff1d-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cff1d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff1d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cff1d-126">INPUTS</span></span>

### <span data-ttu-id="cff1d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cff1d-127">System.String</span></span>

## <span data-ttu-id="cff1d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cff1d-128">OUTPUTS</span></span>

### <span data-ttu-id="cff1d-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cff1d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="cff1d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cff1d-130">NOTES</span></span>

## <span data-ttu-id="cff1d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cff1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="cff1d-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cff1d-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="cff1d-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cff1d-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="cff1d-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cff1d-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cff1d-135">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="cff1d-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
