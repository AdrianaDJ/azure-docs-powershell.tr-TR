---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 9d1b34314c3c620e73a077b77f3935880d6621d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758832"
---
# <span data-ttu-id="0e7f2-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0e7f2-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="0e7f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e7f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7f2-103">Azure SQL Server DNS diğer adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="0e7f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e7f2-104">SYNTAX</span></span>

### <span data-ttu-id="0e7f2-105">Cmdlet Giriş parametrelerinden sunucu DNS diğer adını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0e7f2-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7f2-106">Azuressqlserverdnsaliasmodel örneği tanımından sunucu DNS diğer adlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0e7f2-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7f2-107">Azure kaynak kimliğinden sunucu DNS diğer adını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0e7f2-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7f2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e7f2-108">DESCRIPTION</span></span>
<span data-ttu-id="0e7f2-109">Bu komutlar, sunucudan dokunulmadan Azure SQL Server DNS diğer adını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="0e7f2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e7f2-110">EXAMPLES</span></span>

### <span data-ttu-id="0e7f2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e7f2-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="0e7f2-112">Azure SQL Server DNS diğer adını sunucudan sunucuadı adı adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="0e7f2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e7f2-113">PARAMETERS</span></span>

### <span data-ttu-id="0e7f2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0e7f2-114">-AsJob</span></span>
<span data-ttu-id="0e7f2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0e7f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e7f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7f2-116">-DefaultProfile</span></span>
<span data-ttu-id="0e7f2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e7f2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0e7f2-118">-Force</span></span>
<span data-ttu-id="0e7f2-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="0e7f2-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0e7f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e7f2-120">-InputObject</span></span>
<span data-ttu-id="0e7f2-121">Kaldırılacak sunucu DNS diğer ad nesnesi</span><span class="sxs-lookup"><span data-stu-id="0e7f2-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7f2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e7f2-122">-Name</span></span>
<span data-ttu-id="0e7f2-123">Azure SQL Server DNS diğer adı</span><span class="sxs-lookup"><span data-stu-id="0e7f2-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e7f2-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7f2-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0e7f2-126">-ResourceId</span></span>
<span data-ttu-id="0e7f2-127">Kaldırılacak sunucunun DNS diğer ad nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0e7f2-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7f2-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e7f2-128">-ServerName</span></span>
<span data-ttu-id="0e7f2-129">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7f2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e7f2-130">-Confirm</span></span>
<span data-ttu-id="0e7f2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7f2-132">-WhatIf</span></span>
<span data-ttu-id="0e7f2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7f2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7f2-135">CommonParameters</span></span>
<span data-ttu-id="0e7f2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7f2-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e7f2-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7f2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e7f2-138">INPUTS</span></span>

### <span data-ttu-id="0e7f2-139">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="0e7f2-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="0e7f2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0e7f2-140">System.String</span></span>

## <span data-ttu-id="0e7f2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e7f2-141">OUTPUTS</span></span>

### <span data-ttu-id="0e7f2-142">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="0e7f2-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0e7f2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e7f2-143">NOTES</span></span>

## <span data-ttu-id="0e7f2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e7f2-144">RELATED LINKS</span></span>
