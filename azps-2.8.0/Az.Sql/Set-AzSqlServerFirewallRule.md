---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 5c079adea8079807374d4538f6259cd995103694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933749"
---
# <span data-ttu-id="4d06f-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d06f-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="4d06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d06f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d06f-103">Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="4d06f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d06f-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d06f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d06f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d06f-106">**Set-AzSqlServerFirewallRule** cmdlet 'i, BIR Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="4d06f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d06f-107">EXAMPLES</span></span>

### <span data-ttu-id="4d06f-108">Örnek 1: güvenlik duvarı kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4d06f-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="4d06f-109">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="4d06f-110">Komut başlangıç ve bitiş IP adreslerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="4d06f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d06f-111">PARAMETERS</span></span>

### <span data-ttu-id="4d06f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d06f-112">-DefaultProfile</span></span>
<span data-ttu-id="4d06f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4d06f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d06f-114">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="4d06f-114">-EndIpAddress</span></span>
<span data-ttu-id="4d06f-115">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="4d06f-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="4d06f-116">-FirewallRuleName</span></span>
<span data-ttu-id="4d06f-117">Bu cmdlet 'in değiştirdiği güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4d06f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d06f-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d06f-119">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4d06f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d06f-120">-ServerName</span></span>
<span data-ttu-id="4d06f-121">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4d06f-122">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="4d06f-122">-StartIpAddress</span></span>
<span data-ttu-id="4d06f-123">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="4d06f-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d06f-124">-Confirm</span></span>
<span data-ttu-id="4d06f-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d06f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d06f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d06f-126">-WhatIf</span></span>
<span data-ttu-id="4d06f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d06f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d06f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d06f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d06f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d06f-129">CommonParameters</span></span>
<span data-ttu-id="4d06f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d06f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d06f-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4d06f-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d06f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d06f-132">INPUTS</span></span>

### <span data-ttu-id="4d06f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d06f-133">System.String</span></span>

## <span data-ttu-id="4d06f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d06f-134">OUTPUTS</span></span>

### <span data-ttu-id="4d06f-135">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="4d06f-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="4d06f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d06f-136">NOTES</span></span>

## <span data-ttu-id="4d06f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d06f-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d06f-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d06f-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4d06f-139">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d06f-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4d06f-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4d06f-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4d06f-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="4d06f-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


