---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758877"
---
# <span data-ttu-id="d73a0-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d73a0-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d73a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d73a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d73a0-103">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d73a0-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="d73a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d73a0-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d73a0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d73a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d73a0-106">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d73a0-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="d73a0-107">Azure SQL Server 'daki erişimi yalnızca sanal ağda kullanılabilir olacak şekilde sınırlandırmak için, sanal ağ kuralları, Azure SQL Server 'ı belirli bir sanal ağa bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d73a0-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="d73a0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d73a0-108">EXAMPLES</span></span>

### <span data-ttu-id="d73a0-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d73a0-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="d73a0-110">Azure SQL Server sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="d73a0-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="d73a0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d73a0-111">PARAMETERS</span></span>

### <span data-ttu-id="d73a0-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="d73a0-112">-AsJob</span></span>
<span data-ttu-id="d73a0-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d73a0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d73a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73a0-114">-DefaultProfile</span></span>
<span data-ttu-id="d73a0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d73a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d73a0-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="d73a0-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d73a0-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d73a0-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="d73a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="d73a0-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d73a0-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d73a0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d73a0-120">-ServerName</span></span>
<span data-ttu-id="d73a0-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="d73a0-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d73a0-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d73a0-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d73a0-123">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="d73a0-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="d73a0-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="d73a0-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="d73a0-125">Microsoft. Network ayrıntılarını belirten sanal ağ alt ağı kimliği</span><span class="sxs-lookup"><span data-stu-id="d73a0-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="d73a0-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d73a0-126">-Confirm</span></span>
<span data-ttu-id="d73a0-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d73a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d73a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d73a0-128">-WhatIf</span></span>
<span data-ttu-id="d73a0-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d73a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d73a0-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d73a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d73a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73a0-131">CommonParameters</span></span>
<span data-ttu-id="d73a0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d73a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73a0-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d73a0-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73a0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d73a0-134">INPUTS</span></span>

### <span data-ttu-id="d73a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d73a0-135">System.String</span></span>

## <span data-ttu-id="d73a0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d73a0-136">OUTPUTS</span></span>

### <span data-ttu-id="d73a0-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="d73a0-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d73a0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d73a0-138">NOTES</span></span>

## <span data-ttu-id="d73a0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d73a0-139">RELATED LINKS</span></span>
