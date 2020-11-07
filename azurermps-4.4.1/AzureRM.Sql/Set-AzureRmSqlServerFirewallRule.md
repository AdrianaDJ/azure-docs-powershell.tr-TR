---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765034"
---
# <span data-ttu-id="b60e0-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60e0-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="b60e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b60e0-103">Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b60e0-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b60e0-105">DESCRIPTION</span></span>
<span data-ttu-id="b60e0-106">**Set-AzureRmSqlServerFirewallRule** cmdlet 'i, BIR Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="b60e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b60e0-107">EXAMPLES</span></span>

### <span data-ttu-id="b60e0-108">Örnek 1: güvenlik duvarı kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b60e0-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="b60e0-109">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="b60e0-110">Komut başlangıç ve bitiş IP adreslerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="b60e0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b60e0-111">PARAMETERS</span></span>

### <span data-ttu-id="b60e0-112">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="b60e0-112">-EndIpAddress</span></span>
<span data-ttu-id="b60e0-113">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="b60e0-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b60e0-114">-FirewallRuleName</span></span>
<span data-ttu-id="b60e0-115">Bu cmdlet 'in değiştirdiği güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b60e0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60e0-116">-ResourceGroupName</span></span>
<span data-ttu-id="b60e0-117">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b60e0-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b60e0-118">-ServerName</span></span>
<span data-ttu-id="b60e0-119">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b60e0-120">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="b60e0-120">-StartIpAddress</span></span>
<span data-ttu-id="b60e0-121">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="b60e0-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="b60e0-122">-Confirm</span></span>
<span data-ttu-id="b60e0-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b60e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60e0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60e0-124">-WhatIf</span></span>
<span data-ttu-id="b60e0-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b60e0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60e0-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b60e0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60e0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60e0-127">-DefaultProfile</span></span>
<span data-ttu-id="b60e0-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b60e0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60e0-129">CommonParameters</span></span>
<span data-ttu-id="b60e0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b60e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60e0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60e0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60e0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b60e0-132">INPUTS</span></span>

## <span data-ttu-id="b60e0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b60e0-133">OUTPUTS</span></span>

### <span data-ttu-id="b60e0-134">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="b60e0-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="b60e0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b60e0-135">NOTES</span></span>

## <span data-ttu-id="b60e0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b60e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="b60e0-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60e0-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b60e0-138">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60e0-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b60e0-139">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b60e0-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b60e0-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b60e0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


