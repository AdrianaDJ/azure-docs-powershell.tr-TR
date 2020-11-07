---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937984"
---
# <span data-ttu-id="f9cb7-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9cb7-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="f9cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="f9cb7-103">Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="f9cb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9cb7-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9cb7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="f9cb7-106">Bu komut, Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="f9cb7-107">Sunucudaki sanal ağ kuralları kümesini denetlemek için bunun yerine ' Add-AzSqlServerVirtualNetworkRule ' ve ' Remove-AzSqlServerVirtualNetworkRule ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="f9cb7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9cb7-108">EXAMPLES</span></span>

### <span data-ttu-id="f9cb7-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9cb7-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="f9cb7-110">Yeni sanal ağ hakkında bilgi içeren yeni sanal ağ alt ağı kimliği ile mevcut bir sanal ağ kuralını değiştirir</span><span class="sxs-lookup"><span data-stu-id="f9cb7-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="f9cb7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9cb7-111">PARAMETERS</span></span>

### <span data-ttu-id="f9cb7-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9cb7-112">-AsJob</span></span>
<span data-ttu-id="f9cb7-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9cb7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9cb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9cb7-114">-DefaultProfile</span></span>
<span data-ttu-id="f9cb7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f9cb7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9cb7-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="f9cb7-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f9cb7-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f9cb7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9cb7-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9cb7-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cb7-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9cb7-120">-ServerName</span></span>
<span data-ttu-id="f9cb7-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f9cb7-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="f9cb7-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="f9cb7-123">Azure SQL Server sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="f9cb7-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="f9cb7-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="f9cb7-125">Kuralın sanal ağ alt ağı kimliği.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="f9cb7-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9cb7-126">-Confirm</span></span>
<span data-ttu-id="f9cb7-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9cb7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9cb7-128">-WhatIf</span></span>
<span data-ttu-id="f9cb7-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9cb7-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9cb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9cb7-131">CommonParameters</span></span>
<span data-ttu-id="f9cb7-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9cb7-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f9cb7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9cb7-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9cb7-134">INPUTS</span></span>

### <span data-ttu-id="f9cb7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f9cb7-135">System.String</span></span>

## <span data-ttu-id="f9cb7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9cb7-136">OUTPUTS</span></span>

### <span data-ttu-id="f9cb7-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="f9cb7-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="f9cb7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9cb7-138">NOTES</span></span>

## <span data-ttu-id="f9cb7-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9cb7-139">RELATED LINKS</span></span>
