---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: a1a134905795123311d1ce0fb89e461678f9f41a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931980"
---
# <span data-ttu-id="6ea49-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6ea49-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="6ea49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea49-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea49-103">Genel bir IP öneki alır</span><span class="sxs-lookup"><span data-stu-id="6ea49-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="6ea49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ea49-104">SYNTAX</span></span>

### <span data-ttu-id="6ea49-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ea49-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ea49-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6ea49-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ea49-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea49-108">**Get-AzPublicIpPrefix** cmdlet 'i, kaynak grubunda bir veya birden çok ortak IP önekini alır.</span><span class="sxs-lookup"><span data-stu-id="6ea49-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="6ea49-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ea49-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea49-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ea49-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="6ea49-111">Bu komut, kaynak grubunda myPublicIpPrefix1 ile ortak bir IP önek kaynağı alır myRg</span><span class="sxs-lookup"><span data-stu-id="6ea49-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="6ea49-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ea49-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="6ea49-113">Bu komut, myPublicIpPrefix ile başlayan tüm genel IP öneki kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ea49-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="6ea49-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ea49-114">PARAMETERS</span></span>

### <span data-ttu-id="6ea49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea49-115">-DefaultProfile</span></span>
<span data-ttu-id="6ea49-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ea49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea49-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ea49-117">-Name</span></span>
<span data-ttu-id="6ea49-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6ea49-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6ea49-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea49-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ea49-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6ea49-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6ea49-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ea49-121">-ResourceId</span></span>
<span data-ttu-id="6ea49-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ea49-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea49-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea49-123">CommonParameters</span></span>
<span data-ttu-id="6ea49-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ea49-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea49-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ea49-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea49-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ea49-126">INPUTS</span></span>

### <span data-ttu-id="6ea49-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea49-127">System.String</span></span>

## <span data-ttu-id="6ea49-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ea49-128">OUTPUTS</span></span>

### <span data-ttu-id="6ea49-129">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6ea49-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="6ea49-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ea49-130">NOTES</span></span>

## <span data-ttu-id="6ea49-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ea49-131">RELATED LINKS</span></span>

[<span data-ttu-id="6ea49-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6ea49-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="6ea49-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6ea49-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="6ea49-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6ea49-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
