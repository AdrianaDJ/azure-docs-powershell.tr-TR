---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110233"
---
# <span data-ttu-id="fd730-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fd730-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="fd730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd730-102">SYNOPSIS</span></span>
<span data-ttu-id="fd730-103">Azure SQL Server sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="fd730-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fd730-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd730-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd730-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd730-105">DESCRIPTION</span></span>
<span data-ttu-id="fd730-106">Bu komut bir Azure SQL Server sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="fd730-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fd730-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd730-107">EXAMPLES</span></span>

### <span data-ttu-id="fd730-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd730-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="fd730-109">Var olan bir Azure SQL Server sanal ağ kuralını siler</span><span class="sxs-lookup"><span data-stu-id="fd730-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="fd730-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd730-110">PARAMETERS</span></span>

### <span data-ttu-id="fd730-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="fd730-111">-AsJob</span></span>
<span data-ttu-id="fd730-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fd730-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd730-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd730-113">-DefaultProfile</span></span>
<span data-ttu-id="fd730-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd730-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd730-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd730-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd730-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fd730-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd730-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd730-117">-ServerName</span></span>
<span data-ttu-id="fd730-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="fd730-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fd730-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="fd730-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="fd730-120">Azure SQL Server sanal ağ kuralı adı</span><span class="sxs-lookup"><span data-stu-id="fd730-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="fd730-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd730-121">-Confirm</span></span>
<span data-ttu-id="fd730-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd730-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd730-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd730-123">-WhatIf</span></span>
<span data-ttu-id="fd730-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd730-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd730-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd730-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd730-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd730-126">CommonParameters</span></span>
<span data-ttu-id="fd730-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd730-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd730-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd730-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd730-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd730-129">INPUTS</span></span>

### <span data-ttu-id="fd730-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd730-130">System.String</span></span>

## <span data-ttu-id="fd730-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd730-131">OUTPUTS</span></span>

### <span data-ttu-id="fd730-132">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel</span><span class="sxs-lookup"><span data-stu-id="fd730-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="fd730-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd730-133">NOTES</span></span>

## <span data-ttu-id="fd730-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd730-134">RELATED LINKS</span></span>
