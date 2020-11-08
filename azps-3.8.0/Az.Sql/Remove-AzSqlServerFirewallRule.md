---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098656"
---
# <span data-ttu-id="eeedd-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eeedd-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="eeedd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeedd-102">SYNOPSIS</span></span>
<span data-ttu-id="eeedd-103">SQL veritabanı sunucusundan güvenlik duvarı kuralı siler.</span><span class="sxs-lookup"><span data-stu-id="eeedd-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="eeedd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeedd-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeedd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeedd-105">DESCRIPTION</span></span>
<span data-ttu-id="eeedd-106">**Remove-AzSqlServerFirewallRule** cmdlet 'ı BELIRTILEN Azure SQL veritabanı sunucusundan bir güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="eeedd-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="eeedd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeedd-107">EXAMPLES</span></span>

### <span data-ttu-id="eeedd-108">Örnek 1: kuralı silme</span><span class="sxs-lookup"><span data-stu-id="eeedd-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="eeedd-109">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="eeedd-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="eeedd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeedd-110">PARAMETERS</span></span>

### <span data-ttu-id="eeedd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeedd-111">-DefaultProfile</span></span>
<span data-ttu-id="eeedd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eeedd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeedd-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="eeedd-113">-FirewallRuleName</span></span>
<span data-ttu-id="eeedd-114">Bu cmdlet 'in sildiği güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeedd-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeedd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eeedd-115">-Force</span></span>
<span data-ttu-id="eeedd-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="eeedd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eeedd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeedd-117">-ResourceGroupName</span></span>
<span data-ttu-id="eeedd-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeedd-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eeedd-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eeedd-119">-ServerName</span></span>
<span data-ttu-id="eeedd-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeedd-120">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeedd-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="eeedd-121">-Confirm</span></span>
<span data-ttu-id="eeedd-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eeedd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeedd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeedd-123">-WhatIf</span></span>
<span data-ttu-id="eeedd-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eeedd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeedd-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eeedd-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeedd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeedd-126">CommonParameters</span></span>
<span data-ttu-id="eeedd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeedd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeedd-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eeedd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeedd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeedd-129">INPUTS</span></span>

### <span data-ttu-id="eeedd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eeedd-130">System.String</span></span>

## <span data-ttu-id="eeedd-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeedd-131">OUTPUTS</span></span>

### <span data-ttu-id="eeedd-132">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="eeedd-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="eeedd-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeedd-133">NOTES</span></span>

## <span data-ttu-id="eeedd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeedd-134">RELATED LINKS</span></span>

[<span data-ttu-id="eeedd-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eeedd-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="eeedd-136">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eeedd-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="eeedd-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eeedd-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="eeedd-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="eeedd-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

