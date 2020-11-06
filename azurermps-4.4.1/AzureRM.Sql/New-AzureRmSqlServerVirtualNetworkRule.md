---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587744"
---
# <span data-ttu-id="8f93b-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8f93b-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8f93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f93b-103">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f93b-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f93b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f93b-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f93b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f93b-105">DESCRIPTION</span></span>
<span data-ttu-id="8f93b-106">Azure SQL Server sanal ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f93b-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="8f93b-107">Azure SQL Server 'daki erişimi yalnızca sanal ağda kullanılabilir olacak şekilde sınırlandırmak için, sanal ağ kuralları, Azure SQL Server 'ı belirli bir sanal ağa bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8f93b-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="8f93b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f93b-108">EXAMPLES</span></span>

### <span data-ttu-id="8f93b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f93b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="8f93b-110">Azure SQL Server sanal ağ kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8f93b-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="8f93b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f93b-111">PARAMETERS</span></span>

### <span data-ttu-id="8f93b-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f93b-112">-ResourceGroupName</span></span>
<span data-ttu-id="8f93b-113">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8f93b-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f93b-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f93b-114">-ServerName</span></span>
<span data-ttu-id="8f93b-115">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="8f93b-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8f93b-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8f93b-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8f93b-117">Azure SQL Server sanal ağ kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="8f93b-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="8f93b-118">-Virtualnetworksubnetıd</span><span class="sxs-lookup"><span data-stu-id="8f93b-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="8f93b-119">Microsoft. Network ayrıntılarını belirten sanal ağ alt ağı kimliği</span><span class="sxs-lookup"><span data-stu-id="8f93b-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="8f93b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f93b-120">-Confirm</span></span>
<span data-ttu-id="8f93b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f93b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f93b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f93b-122">-WhatIf</span></span>
<span data-ttu-id="8f93b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f93b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f93b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f93b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f93b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f93b-125">-DefaultProfile</span></span>
<span data-ttu-id="8f93b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f93b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f93b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f93b-127">CommonParameters</span></span>
<span data-ttu-id="8f93b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f93b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f93b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f93b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f93b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f93b-130">INPUTS</span></span>

### <span data-ttu-id="8f93b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8f93b-131">System.String</span></span>

## <span data-ttu-id="8f93b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f93b-132">OUTPUTS</span></span>

### <span data-ttu-id="8f93b-133">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="8f93b-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8f93b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f93b-134">NOTES</span></span>

## <span data-ttu-id="8f93b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f93b-135">RELATED LINKS</span></span>

