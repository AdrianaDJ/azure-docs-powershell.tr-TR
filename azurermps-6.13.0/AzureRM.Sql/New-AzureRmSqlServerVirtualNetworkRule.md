---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c2e3386d7c9146eeaa96220ddcbea4cf50864e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587136"
---
# <span data-ttu-id="a242f-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a242f-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a242f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a242f-102">SYNOPSIS</span></span>
<span data-ttu-id="a242f-103">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a242f-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a242f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a242f-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a242f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a242f-105">DESCRIPTION</span></span>
<span data-ttu-id="a242f-106">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a242f-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="a242f-107">Azure SQL Server 'daki erişimi yalnızca sanal ağda kullanılabilir olacak şekilde sınırlandırmak için, sanal ağ kuralları, Azure SQL Server 'ı belirli bir sanal ağa bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a242f-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="a242f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a242f-108">EXAMPLES</span></span>

### <span data-ttu-id="a242f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a242f-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="a242f-110">Azure SQL Server sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="a242f-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="a242f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a242f-111">PARAMETERS</span></span>

### <span data-ttu-id="a242f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="a242f-112">-AsJob</span></span>
<span data-ttu-id="a242f-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a242f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a242f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a242f-114">-DefaultProfile</span></span>
<span data-ttu-id="a242f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a242f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a242f-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="a242f-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a242f-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a242f-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a242f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a242f-118">-ResourceGroupName</span></span>
<span data-ttu-id="a242f-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a242f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="a242f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a242f-120">-ServerName</span></span>
<span data-ttu-id="a242f-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="a242f-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a242f-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a242f-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a242f-123">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="a242f-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="a242f-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="a242f-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="a242f-125">Microsoft. Network ayrıntılarını belirten sanal ağ alt ağı kimliği</span><span class="sxs-lookup"><span data-stu-id="a242f-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="a242f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a242f-126">-Confirm</span></span>
<span data-ttu-id="a242f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a242f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a242f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a242f-128">-WhatIf</span></span>
<span data-ttu-id="a242f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a242f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a242f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a242f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a242f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a242f-131">CommonParameters</span></span>
<span data-ttu-id="a242f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a242f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a242f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a242f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a242f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a242f-134">INPUTS</span></span>

### <span data-ttu-id="a242f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a242f-135">System.String</span></span>

## <span data-ttu-id="a242f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a242f-136">OUTPUTS</span></span>

### <span data-ttu-id="a242f-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="a242f-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a242f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a242f-138">NOTES</span></span>

## <span data-ttu-id="a242f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a242f-139">RELATED LINKS</span></span>
