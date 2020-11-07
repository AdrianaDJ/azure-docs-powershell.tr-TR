---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762828"
---
# <span data-ttu-id="08d1b-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="08d1b-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="08d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="08d1b-103">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08d1b-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08d1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08d1b-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="08d1b-106">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08d1b-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="08d1b-107">Azure SQL Server 'daki erişimi yalnızca sanal ağda kullanılabilir olacak şekilde sınırlandırmak için, sanal ağ kuralları, Azure SQL Server 'ı belirli bir sanal ağa bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08d1b-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="08d1b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08d1b-108">EXAMPLES</span></span>

### <span data-ttu-id="08d1b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08d1b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="08d1b-110">Azure SQL Server sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d1b-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="08d1b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08d1b-111">PARAMETERS</span></span>

### <span data-ttu-id="08d1b-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="08d1b-112">-AsJob</span></span>
<span data-ttu-id="08d1b-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="08d1b-113">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d1b-114">-DefaultProfile</span></span>
<span data-ttu-id="08d1b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="08d1b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="08d1b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="08d1b-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="08d1b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="08d1b-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08d1b-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08d1b-120">-ServerName</span></span>
<span data-ttu-id="08d1b-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="08d1b-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="08d1b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="08d1b-123">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="08d1b-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="08d1b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="08d1b-125">Microsoft. Network ayrıntılarını belirten sanal ağ alt ağı kimliği</span><span class="sxs-lookup"><span data-stu-id="08d1b-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="08d1b-126">-Confirm</span></span>
<span data-ttu-id="08d1b-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08d1b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d1b-128">-WhatIf</span></span>
<span data-ttu-id="08d1b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08d1b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d1b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08d1b-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d1b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d1b-131">CommonParameters</span></span>
<span data-ttu-id="08d1b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08d1b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d1b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d1b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d1b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08d1b-134">INPUTS</span></span>

### <span data-ttu-id="08d1b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="08d1b-135">System.String</span></span>

## <span data-ttu-id="08d1b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08d1b-136">OUTPUTS</span></span>

### <span data-ttu-id="08d1b-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="08d1b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="08d1b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08d1b-138">NOTES</span></span>

## <span data-ttu-id="08d1b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08d1b-139">RELATED LINKS</span></span>
