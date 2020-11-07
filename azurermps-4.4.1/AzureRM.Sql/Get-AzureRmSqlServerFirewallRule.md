---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763604"
---
# <span data-ttu-id="0ae16-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ae16-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="0ae16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae16-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae16-103">SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="0ae16-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ae16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ae16-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ae16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ae16-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae16-106">**Get-AzureRmSqlServerFirewallRule** cmdlet 'i, BIR Azure SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="0ae16-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="0ae16-107">Güvenlik duvarının adını belirtirseniz, bu cmdlet ilgili güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0ae16-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="0ae16-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ae16-108">EXAMPLES</span></span>

### <span data-ttu-id="0ae16-109">Örnek 1: sunucunun tüm kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="0ae16-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="0ae16-110">Bu komut, server01 adındaki sunucunun tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="0ae16-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="0ae16-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ae16-111">PARAMETERS</span></span>

### <span data-ttu-id="0ae16-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="0ae16-112">-FirewallRuleName</span></span>
<span data-ttu-id="0ae16-113">Güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ae16-113">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="0ae16-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae16-114">-ResourceGroupName</span></span>
<span data-ttu-id="0ae16-115">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ae16-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="0ae16-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0ae16-116">-ServerName</span></span>
<span data-ttu-id="0ae16-117">SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ae16-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="0ae16-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ae16-118">-Confirm</span></span>
<span data-ttu-id="0ae16-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ae16-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ae16-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ae16-120">-WhatIf</span></span>
<span data-ttu-id="0ae16-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ae16-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ae16-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ae16-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ae16-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae16-123">-DefaultProfile</span></span>
<span data-ttu-id="0ae16-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ae16-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ae16-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae16-125">CommonParameters</span></span>
<span data-ttu-id="0ae16-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ae16-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae16-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae16-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae16-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ae16-128">INPUTS</span></span>

## <span data-ttu-id="0ae16-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ae16-129">OUTPUTS</span></span>

### <span data-ttu-id="0ae16-130">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="0ae16-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="0ae16-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ae16-131">NOTES</span></span>

## <span data-ttu-id="0ae16-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ae16-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ae16-133">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ae16-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ae16-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ae16-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ae16-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ae16-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="0ae16-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0ae16-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


