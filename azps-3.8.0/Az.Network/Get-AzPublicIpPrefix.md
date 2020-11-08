---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098776"
---
# <span data-ttu-id="340e1-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="340e1-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="340e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340e1-102">SYNOPSIS</span></span>
<span data-ttu-id="340e1-103">Genel bir IP öneki alır</span><span class="sxs-lookup"><span data-stu-id="340e1-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="340e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="340e1-104">SYNTAX</span></span>

### <span data-ttu-id="340e1-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="340e1-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="340e1-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="340e1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="340e1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="340e1-107">DESCRIPTION</span></span>
<span data-ttu-id="340e1-108">**Get-AzPublicIpPrefix** cmdlet 'i, kaynak grubunda bir veya birden çok ortak IP önekini alır.</span><span class="sxs-lookup"><span data-stu-id="340e1-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="340e1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="340e1-109">EXAMPLES</span></span>

### <span data-ttu-id="340e1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="340e1-110">Example 1</span></span>
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

<span data-ttu-id="340e1-111">Bu komut, kaynak grubunda myPublicIpPrefix1 ile ortak bir IP önek kaynağı alır myRg</span><span class="sxs-lookup"><span data-stu-id="340e1-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="340e1-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="340e1-112">Example 2</span></span>
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

<span data-ttu-id="340e1-113">Bu komut, myPublicIpPrefix ile başlayan tüm genel IP öneki kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="340e1-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="340e1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="340e1-114">PARAMETERS</span></span>

### <span data-ttu-id="340e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340e1-115">-DefaultProfile</span></span>
<span data-ttu-id="340e1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="340e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340e1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="340e1-117">-Name</span></span>
<span data-ttu-id="340e1-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="340e1-118">The resource name.</span></span>

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

### <span data-ttu-id="340e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="340e1-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="340e1-120">The resource group name.</span></span>

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

### <span data-ttu-id="340e1-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="340e1-121">-ResourceId</span></span>
<span data-ttu-id="340e1-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="340e1-122">The resource Id.</span></span>

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

### <span data-ttu-id="340e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340e1-123">CommonParameters</span></span>
<span data-ttu-id="340e1-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="340e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340e1-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="340e1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340e1-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="340e1-126">INPUTS</span></span>

### <span data-ttu-id="340e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="340e1-127">System.String</span></span>

## <span data-ttu-id="340e1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="340e1-128">OUTPUTS</span></span>

### <span data-ttu-id="340e1-129">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="340e1-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="340e1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="340e1-130">NOTES</span></span>

## <span data-ttu-id="340e1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="340e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="340e1-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="340e1-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="340e1-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="340e1-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="340e1-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="340e1-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
