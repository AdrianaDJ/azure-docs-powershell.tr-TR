---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278580"
---
# <span data-ttu-id="5303c-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5303c-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5303c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5303c-102">SYNOPSIS</span></span>
<span data-ttu-id="5303c-103">Özel DNS bölgesi grubunu alır</span><span class="sxs-lookup"><span data-stu-id="5303c-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="5303c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5303c-104">SYNTAX</span></span>

### <span data-ttu-id="5303c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5303c-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5303c-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="5303c-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5303c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5303c-107">DESCRIPTION</span></span>
<span data-ttu-id="5303c-108">**Get-AzPrivateDnsZoneGroup** cmdlet 'i bir veya daha çok özel DNS bölge grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="5303c-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="5303c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5303c-109">EXAMPLES</span></span>

### <span data-ttu-id="5303c-110">Örnek 1: özel DNS bölge grubunu alma</span><span class="sxs-lookup"><span data-stu-id="5303c-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="5303c-111">Yukarıdaki örnek, kaynak grubundaki dnsgroup1 adlı özel bir DNS bölgesi grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="5303c-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="5303c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5303c-112">PARAMETERS</span></span>

### <span data-ttu-id="5303c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5303c-113">-DefaultProfile</span></span>
<span data-ttu-id="5303c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5303c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5303c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5303c-115">-Name</span></span>
<span data-ttu-id="5303c-116">Özel DNS bölgesi grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5303c-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5303c-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5303c-117">-PrivateEndpointName</span></span>
<span data-ttu-id="5303c-118">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="5303c-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5303c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5303c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5303c-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5303c-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5303c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5303c-121">CommonParameters</span></span>
<span data-ttu-id="5303c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5303c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5303c-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5303c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5303c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5303c-124">INPUTS</span></span>

### <span data-ttu-id="5303c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5303c-125">System.String</span></span>

## <span data-ttu-id="5303c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5303c-126">OUTPUTS</span></span>

### <span data-ttu-id="5303c-127">Microsoft. Azure. Commands. Network. model. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5303c-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5303c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5303c-128">NOTES</span></span>

## <span data-ttu-id="5303c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5303c-129">RELATED LINKS</span></span>
