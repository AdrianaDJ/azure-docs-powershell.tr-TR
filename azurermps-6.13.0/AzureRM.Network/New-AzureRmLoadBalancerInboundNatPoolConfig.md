---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 097377cd1ca4cb4be4fe62e2008f899c05c194fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594371"
---
# <span data-ttu-id="6caea-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6caea-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="6caea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6caea-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6caea-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6caea-103">SYNTAX</span></span>

### <span data-ttu-id="6caea-104">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6caea-104">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6caea-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6caea-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6caea-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6caea-106">DESCRIPTION</span></span>

## <span data-ttu-id="6caea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6caea-107">EXAMPLES</span></span>

### <span data-ttu-id="6caea-108">1: yeni</span><span class="sxs-lookup"><span data-stu-id="6caea-108">1: New</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="6caea-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6caea-109">PARAMETERS</span></span>

### <span data-ttu-id="6caea-110">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6caea-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6caea-111">-DefaultProfile</span></span>
<span data-ttu-id="6caea-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6caea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6caea-113">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6caea-113">-EnableFloatingIP</span></span>
<span data-ttu-id="6caea-114">SQL AlwaysOn kullanılabilirlik grubunu yapılandırmak için gereken kayan IP yeteneği için sanal makinenin uç noktasını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6caea-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="6caea-115">SQL Server 'da SQL AlwaysOn kullanılabilirlik grupları kullanılırken bu ayar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6caea-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="6caea-116">Uç noktayı oluşturduktan sonra bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="6caea-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="6caea-117">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="6caea-117">-EnableTcpReset</span></span>
<span data-ttu-id="6caea-118">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="6caea-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6caea-119">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6caea-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6caea-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6caea-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-121">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6caea-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-122">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="6caea-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-123">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="6caea-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-124">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6caea-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6caea-125">TCP boştaki bağlantı için zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="6caea-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="6caea-126">Değer 4 ile 30 dakika arasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6caea-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="6caea-127">Varsayılan değer 4 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="6caea-127">The default value is 4 minutes.</span></span> <span data-ttu-id="6caea-128">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6caea-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="6caea-129">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6caea-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6caea-130">-Protocol</span></span>
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

### <span data-ttu-id="6caea-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6caea-131">-Confirm</span></span>
<span data-ttu-id="6caea-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6caea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6caea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6caea-133">-WhatIf</span></span>
<span data-ttu-id="6caea-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6caea-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6caea-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6caea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6caea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6caea-136">CommonParameters</span></span>
<span data-ttu-id="6caea-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6caea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6caea-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6caea-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6caea-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6caea-139">INPUTS</span></span>

### <span data-ttu-id="6caea-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6caea-140">None</span></span>

## <span data-ttu-id="6caea-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6caea-141">OUTPUTS</span></span>

### <span data-ttu-id="6caea-142">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="6caea-142">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="6caea-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6caea-143">NOTES</span></span>

## <span data-ttu-id="6caea-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6caea-144">RELATED LINKS</span></span>
