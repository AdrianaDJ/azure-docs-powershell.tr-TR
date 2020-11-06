---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c71f8284cc3b1a2648e3523c77f0e9e2dd2d3876
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589297"
---
# <span data-ttu-id="b9827-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9827-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b9827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9827-102">SYNOPSIS</span></span>
<span data-ttu-id="b9827-103">Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b9827-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9827-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9827-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9827-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9827-105">DESCRIPTION</span></span>
<span data-ttu-id="b9827-106">Bu komut, Azure SQL Server sanal ağ kuralının yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b9827-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b9827-107">Sunucudaki sanal ağ kuralları kümesini denetlemek için bunun yerine ' Add-AzureRmSqlServerVirtualNetworkRule ' ve ' Remove-AzureRmSqlServerVirtualNetworkRule ' seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9827-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b9827-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9827-108">EXAMPLES</span></span>

### <span data-ttu-id="b9827-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9827-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b9827-110">Yeni sanal ağ hakkında bilgi içeren yeni sanal ağ alt ağı kimliği ile mevcut bir sanal ağ kuralını değiştirir</span><span class="sxs-lookup"><span data-stu-id="b9827-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b9827-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9827-111">PARAMETERS</span></span>

### <span data-ttu-id="b9827-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="b9827-112">-AsJob</span></span>
<span data-ttu-id="b9827-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b9827-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9827-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9827-114">-DefaultProfile</span></span>
<span data-ttu-id="b9827-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b9827-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9827-116">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="b9827-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b9827-117">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b9827-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b9827-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9827-118">-ResourceGroupName</span></span>
<span data-ttu-id="b9827-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b9827-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9827-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9827-120">-ServerName</span></span>
<span data-ttu-id="b9827-121">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="b9827-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b9827-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b9827-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b9827-123">Azure SQL Server sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="b9827-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b9827-124">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="b9827-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b9827-125">Kuralın sanal ağ alt ağı kimliği.</span><span class="sxs-lookup"><span data-stu-id="b9827-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b9827-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9827-126">-Confirm</span></span>
<span data-ttu-id="b9827-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9827-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9827-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9827-128">-WhatIf</span></span>
<span data-ttu-id="b9827-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9827-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9827-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9827-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9827-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9827-131">CommonParameters</span></span>
<span data-ttu-id="b9827-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9827-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9827-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9827-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9827-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9827-134">INPUTS</span></span>

### <span data-ttu-id="b9827-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b9827-135">System.String</span></span>

## <span data-ttu-id="b9827-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9827-136">OUTPUTS</span></span>

### <span data-ttu-id="b9827-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="b9827-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b9827-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9827-138">NOTES</span></span>

## <span data-ttu-id="b9827-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9827-139">RELATED LINKS</span></span>
