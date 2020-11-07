---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760020"
---
# <span data-ttu-id="77e6f-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="77e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="77e6f-103">ExpressRoute çapraz bağlantısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="77e6f-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="77e6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77e6f-104">SYNTAX</span></span>

### <span data-ttu-id="77e6f-105">Modifybydevresi başvurusu</span><span class="sxs-lookup"><span data-stu-id="77e6f-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e6f-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="77e6f-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e6f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="77e6f-107">DESCRIPTION</span></span>
<span data-ttu-id="77e6f-108">**Set-AzExpressRouteCrossConnection** cmdlet 'i Azure 'A değiştirilmiş ExpressRoute çapraz bağlantısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="77e6f-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="77e6f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77e6f-109">EXAMPLES</span></span>

### <span data-ttu-id="77e6f-110">Örnek 1: ExpressRoute çapraz bağlantısının hizmet sağlayıcısı sağlama durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="77e6f-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="77e6f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77e6f-111">PARAMETERS</span></span>

### <span data-ttu-id="77e6f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="77e6f-112">-AsJob</span></span>
<span data-ttu-id="77e6f-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="77e6f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77e6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e6f-114">-DefaultProfile</span></span>
<span data-ttu-id="77e6f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77e6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e6f-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="77e6f-117">Bu cmdlet 'in değiştirdiği **Expressroutecrossconnection** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77e6f-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="77e6f-118">-Force</span></span>
<span data-ttu-id="77e6f-119">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="77e6f-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="77e6f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="77e6f-120">-Name</span></span>
<span data-ttu-id="77e6f-121">Hızlı yol çapraz bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="77e6f-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-122">-Peering</span><span class="sxs-lookup"><span data-stu-id="77e6f-122">-Peerings</span></span>
<span data-ttu-id="77e6f-123">Çapraz bağlantı için eş bağlantılar listesi</span><span class="sxs-lookup"><span data-stu-id="77e6f-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="77e6f-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="77e6f-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="77e6f-127">Hizmet sağlayıcı notları</span><span class="sxs-lookup"><span data-stu-id="77e6f-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="77e6f-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="77e6f-129">Ayarlanacak hizmet sağlayıcısı sağlama durumu</span><span class="sxs-lookup"><span data-stu-id="77e6f-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e6f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="77e6f-130">-Confirm</span></span>
<span data-ttu-id="77e6f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77e6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e6f-132">-WhatIf</span></span>
<span data-ttu-id="77e6f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77e6f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77e6f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77e6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e6f-135">CommonParameters</span></span>
<span data-ttu-id="77e6f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77e6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e6f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e6f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e6f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77e6f-138">INPUTS</span></span>

### <span data-ttu-id="77e6f-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="77e6f-140">' ExpressRouteCrossConnection ' parametresi ardışık düzenin ' PSExpressRouteCrossConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="77e6f-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="77e6f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77e6f-141">OUTPUTS</span></span>

### <span data-ttu-id="77e6f-142">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="77e6f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77e6f-143">NOTES</span></span>

## <span data-ttu-id="77e6f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77e6f-144">RELATED LINKS</span></span>

[<span data-ttu-id="77e6f-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="77e6f-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
