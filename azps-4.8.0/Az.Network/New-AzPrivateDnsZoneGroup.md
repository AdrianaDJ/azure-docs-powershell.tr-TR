---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109461"
---
# <span data-ttu-id="dfef0-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="dfef0-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="dfef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfef0-102">SYNOPSIS</span></span>
<span data-ttu-id="dfef0-103">Belirtilen özel uç noktada özel bir DNS bölge grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfef0-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="dfef0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfef0-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfef0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfef0-105">DESCRIPTION</span></span>
<span data-ttu-id="dfef0-106">**New-AzPrivateDnsZoneGroup** cmdlet 'i, yeni BIR özel DNS bölge grubu oluşturmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="dfef0-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="dfef0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfef0-107">EXAMPLES</span></span>

### <span data-ttu-id="dfef0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dfef0-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
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

<span data-ttu-id="dfef0-109">Özel uç nokta `test-pr-endpoint` oluşturulduktan sonra, yukarıdaki örnek, bu özel uç nokta altında DNS bölge grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dfef0-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="dfef0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfef0-110">PARAMETERS</span></span>

### <span data-ttu-id="dfef0-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="dfef0-111">-AsJob</span></span>
<span data-ttu-id="dfef0-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dfef0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfef0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfef0-113">-DefaultProfile</span></span>
<span data-ttu-id="dfef0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfef0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfef0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dfef0-115">-Force</span></span>
<span data-ttu-id="dfef0-116">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="dfef0-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dfef0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="dfef0-117">-Name</span></span>
<span data-ttu-id="dfef0-118">Özel DNS bölgesi grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dfef0-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="dfef0-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="dfef0-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="dfef0-120">Özel DNS bölgesi grubunun özel DNS bölgesi yapılandırmaları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="dfef0-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="dfef0-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="dfef0-121">-PrivateEndpointName</span></span>
<span data-ttu-id="dfef0-122">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="dfef0-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="dfef0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfef0-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfef0-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dfef0-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfef0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="dfef0-125">-Confirm</span></span>
<span data-ttu-id="dfef0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dfef0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfef0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfef0-127">-WhatIf</span></span>
<span data-ttu-id="dfef0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dfef0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfef0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfef0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfef0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfef0-130">CommonParameters</span></span>
<span data-ttu-id="dfef0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfef0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfef0-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dfef0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfef0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfef0-133">INPUTS</span></span>

### <span data-ttu-id="dfef0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dfef0-134">System.String</span></span>

### <span data-ttu-id="dfef0-135">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Psprivatednszonezone, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dfef0-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dfef0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfef0-136">OUTPUTS</span></span>

### <span data-ttu-id="dfef0-137">Microsoft. Azure. Commands. Network. model. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="dfef0-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="dfef0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfef0-138">NOTES</span></span>

## <span data-ttu-id="dfef0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfef0-139">RELATED LINKS</span></span>
