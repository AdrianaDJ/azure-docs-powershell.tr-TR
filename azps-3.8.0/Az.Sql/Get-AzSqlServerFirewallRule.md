---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937317"
---
# <span data-ttu-id="a2cff-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2cff-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="a2cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2cff-102">SYNOPSIS</span></span>
<span data-ttu-id="a2cff-103">SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2cff-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="a2cff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2cff-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2cff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2cff-105">DESCRIPTION</span></span>
<span data-ttu-id="a2cff-106">**Get-AzSqlServerFirewallRule** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2cff-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="a2cff-107">Güvenlik duvarının adını belirtirseniz, bu cmdlet ilgili güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a2cff-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="a2cff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2cff-108">EXAMPLES</span></span>

### <span data-ttu-id="a2cff-109">Örnek 1: sunucunun tüm kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="a2cff-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="a2cff-110">Bu komut, server01 adındaki sunucunun tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2cff-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="a2cff-111">Örnek 2: filtreleme kullanarak sunucunun tüm kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="a2cff-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="a2cff-112">Bu komut, server01 adlı sunucunun "Rule" ile başlayan tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a2cff-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="a2cff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2cff-113">PARAMETERS</span></span>

### <span data-ttu-id="a2cff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2cff-114">-DefaultProfile</span></span>
<span data-ttu-id="a2cff-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a2cff-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2cff-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a2cff-116">-FirewallRuleName</span></span>
<span data-ttu-id="a2cff-117">Güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2cff-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2cff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2cff-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2cff-119">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2cff-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="a2cff-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2cff-120">-ServerName</span></span>
<span data-ttu-id="a2cff-121">SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2cff-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="a2cff-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2cff-122">-Confirm</span></span>
<span data-ttu-id="a2cff-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2cff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2cff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2cff-124">-WhatIf</span></span>
<span data-ttu-id="a2cff-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2cff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2cff-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2cff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2cff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2cff-127">CommonParameters</span></span>
<span data-ttu-id="a2cff-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2cff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2cff-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2cff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2cff-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2cff-130">INPUTS</span></span>

### <span data-ttu-id="a2cff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a2cff-131">System.String</span></span>

## <span data-ttu-id="a2cff-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2cff-132">OUTPUTS</span></span>

### <span data-ttu-id="a2cff-133">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="a2cff-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a2cff-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2cff-134">NOTES</span></span>

## <span data-ttu-id="a2cff-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2cff-135">RELATED LINKS</span></span>

[<span data-ttu-id="a2cff-136">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2cff-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a2cff-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2cff-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a2cff-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a2cff-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a2cff-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a2cff-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

