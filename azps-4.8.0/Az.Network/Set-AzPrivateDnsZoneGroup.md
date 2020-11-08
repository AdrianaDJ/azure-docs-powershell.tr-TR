---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265901"
---
# <span data-ttu-id="f07f8-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f07f8-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="f07f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f07f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f07f8-103">DNS bölgesi grubunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f07f8-103">Updates DNS zone group</span></span>

## <span data-ttu-id="f07f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f07f8-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f07f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f07f8-106">**Set-AzPrivateDnsZoneGroup** CMDLET 'i DNS bölge grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f07f8-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="f07f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f07f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f07f8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f07f8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="f07f8-109">Yukarıdaki örnekte, dnsgroup1 adlı DNS bölgesi, başka bir DNS bölgesine bağlanan yeni bir dnsconfig ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f07f8-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="f07f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f07f8-110">PARAMETERS</span></span>

### <span data-ttu-id="f07f8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f07f8-111">-AsJob</span></span>
<span data-ttu-id="f07f8-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f07f8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07f8-113">-DefaultProfile</span></span>
<span data-ttu-id="f07f8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f07f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f07f8-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f07f8-115">-Name</span></span>
<span data-ttu-id="f07f8-116">Özel DNS bölgesi grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f07f8-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f07f8-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="f07f8-118">Özel DNS bölgesi grubunun özel DNS bölgesi yapılandırmaları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="f07f8-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="f07f8-119">-PrivateEndpointName</span></span>
<span data-ttu-id="f07f8-120">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="f07f8-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="f07f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="f07f8-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f07f8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f07f8-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f07f8-123">-Confirm</span></span>
<span data-ttu-id="f07f8-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f07f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07f8-125">-WhatIf</span></span>
<span data-ttu-id="f07f8-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f07f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07f8-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f07f8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07f8-128">CommonParameters</span></span>
<span data-ttu-id="f07f8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f07f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07f8-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f07f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07f8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f07f8-131">INPUTS</span></span>

### <span data-ttu-id="f07f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f07f8-132">System.String</span></span>

### <span data-ttu-id="f07f8-133">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Psprivatednszonezone, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f07f8-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f07f8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f07f8-134">OUTPUTS</span></span>

### <span data-ttu-id="f07f8-135">Microsoft. Azure. Commands. Network. model. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f07f8-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="f07f8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f07f8-136">NOTES</span></span>

## <span data-ttu-id="f07f8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f07f8-137">RELATED LINKS</span></span>
