---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 5e32e136d293c7b5eb8017592cf1ac4e01c60b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590003"
---
# <span data-ttu-id="b5afd-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5afd-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="b5afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5afd-102">SYNOPSIS</span></span>
<span data-ttu-id="b5afd-103">SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5afd-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5afd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5afd-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5afd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5afd-105">DESCRIPTION</span></span>
<span data-ttu-id="b5afd-106">**Get-AzureRmSqlServerFirewallRule** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5afd-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="b5afd-107">Güvenlik duvarının adını belirtirseniz, bu cmdlet ilgili güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b5afd-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="b5afd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5afd-108">EXAMPLES</span></span>

### <span data-ttu-id="b5afd-109">Örnek 1: sunucunun tüm kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="b5afd-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="b5afd-110">Bu komut, server01 adındaki sunucunun tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5afd-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="b5afd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5afd-111">PARAMETERS</span></span>

### <span data-ttu-id="b5afd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5afd-112">-DefaultProfile</span></span>
<span data-ttu-id="b5afd-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b5afd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5afd-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b5afd-114">-FirewallRuleName</span></span>
<span data-ttu-id="b5afd-115">Güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5afd-115">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="b5afd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5afd-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5afd-117">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5afd-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="b5afd-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5afd-118">-ServerName</span></span>
<span data-ttu-id="b5afd-119">SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5afd-119">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="b5afd-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5afd-120">-Confirm</span></span>
<span data-ttu-id="b5afd-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5afd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5afd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5afd-122">-WhatIf</span></span>
<span data-ttu-id="b5afd-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5afd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5afd-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5afd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5afd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5afd-125">CommonParameters</span></span>
<span data-ttu-id="b5afd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5afd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5afd-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5afd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5afd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5afd-128">INPUTS</span></span>

### <span data-ttu-id="b5afd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b5afd-129">System.String</span></span>

## <span data-ttu-id="b5afd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5afd-130">OUTPUTS</span></span>

### <span data-ttu-id="b5afd-131">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="b5afd-131">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="b5afd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5afd-132">NOTES</span></span>

## <span data-ttu-id="b5afd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5afd-133">RELATED LINKS</span></span>

[<span data-ttu-id="b5afd-134">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5afd-134">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b5afd-135">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5afd-135">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b5afd-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5afd-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b5afd-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b5afd-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


