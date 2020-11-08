---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276655"
---
# <span data-ttu-id="3c768-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3c768-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3c768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c768-102">SYNOPSIS</span></span>
<span data-ttu-id="3c768-103">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c768-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="3c768-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c768-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c768-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c768-105">DESCRIPTION</span></span>
<span data-ttu-id="3c768-106">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c768-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="3c768-107">Azure SQL Server 'daki erişimi yalnızca sanal ağda kullanılabilir olacak şekilde sınırlandırmak için, sanal ağ kuralları, Azure SQL Server 'ı belirli bir sanal ağa bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3c768-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="3c768-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c768-108">EXAMPLES</span></span>

### <span data-ttu-id="3c768-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c768-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="3c768-110">Azure SQL Server sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3c768-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="3c768-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c768-111">PARAMETERS</span></span>

### <span data-ttu-id="3c768-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="3c768-112">-AsJob</span></span>
<span data-ttu-id="3c768-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3c768-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c768-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c768-114">-DefaultProfile</span></span>
<span data-ttu-id="3c768-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3c768-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c768-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="3c768-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3c768-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3c768-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3c768-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c768-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c768-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3c768-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c768-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c768-120">-ServerName</span></span>
<span data-ttu-id="3c768-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="3c768-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3c768-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3c768-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3c768-123">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="3c768-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="3c768-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="3c768-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="3c768-125">Microsoft. Network ayrıntılarını belirten sanal ağ alt ağı kimliği</span><span class="sxs-lookup"><span data-stu-id="3c768-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="3c768-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c768-126">-Confirm</span></span>
<span data-ttu-id="3c768-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c768-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c768-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c768-128">-WhatIf</span></span>
<span data-ttu-id="3c768-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c768-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c768-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c768-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c768-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c768-131">CommonParameters</span></span>
<span data-ttu-id="3c768-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c768-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c768-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c768-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c768-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c768-134">INPUTS</span></span>

### <span data-ttu-id="3c768-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3c768-135">System.String</span></span>

## <span data-ttu-id="3c768-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c768-136">OUTPUTS</span></span>

### <span data-ttu-id="3c768-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="3c768-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3c768-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c768-138">NOTES</span></span>

## <span data-ttu-id="3c768-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c768-139">RELATED LINKS</span></span>
