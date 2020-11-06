---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588728"
---
# <span data-ttu-id="f731d-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f731d-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="f731d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f731d-102">SYNOPSIS</span></span>
<span data-ttu-id="f731d-103">SQL veritabanı sunucusundan güvenlik duvarı kuralı siler.</span><span class="sxs-lookup"><span data-stu-id="f731d-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f731d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f731d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f731d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f731d-105">DESCRIPTION</span></span>
<span data-ttu-id="f731d-106">**Remove-AzureRmSqlServerFirewallRule** cmdlet 'ı BELIRTILEN Azure SQL veritabanı sunucusundan bir güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="f731d-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="f731d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f731d-107">EXAMPLES</span></span>

### <span data-ttu-id="f731d-108">Örnek 1: kuralı silme</span><span class="sxs-lookup"><span data-stu-id="f731d-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f731d-109">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="f731d-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="f731d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f731d-110">PARAMETERS</span></span>

### <span data-ttu-id="f731d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f731d-111">-DefaultProfile</span></span>
<span data-ttu-id="f731d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f731d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f731d-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f731d-113">-FirewallRuleName</span></span>
<span data-ttu-id="f731d-114">Bu cmdlet 'in sildiği güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f731d-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f731d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f731d-115">-Force</span></span>
<span data-ttu-id="f731d-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f731d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f731d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f731d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f731d-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f731d-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f731d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f731d-119">-ServerName</span></span>
<span data-ttu-id="f731d-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f731d-120">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f731d-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f731d-121">-Confirm</span></span>
<span data-ttu-id="f731d-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f731d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f731d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f731d-123">-WhatIf</span></span>
<span data-ttu-id="f731d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f731d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f731d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f731d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f731d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f731d-126">CommonParameters</span></span>
<span data-ttu-id="f731d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f731d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f731d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f731d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f731d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f731d-129">INPUTS</span></span>

### <span data-ttu-id="f731d-130">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="f731d-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f731d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f731d-131">OUTPUTS</span></span>

## <span data-ttu-id="f731d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f731d-132">NOTES</span></span>

## <span data-ttu-id="f731d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f731d-133">RELATED LINKS</span></span>

[<span data-ttu-id="f731d-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f731d-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f731d-135">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f731d-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f731d-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f731d-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f731d-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f731d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


