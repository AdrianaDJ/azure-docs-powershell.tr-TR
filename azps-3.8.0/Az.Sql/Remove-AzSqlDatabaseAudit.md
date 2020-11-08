---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937310"
---
# <span data-ttu-id="83e2a-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="83e2a-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="83e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="83e2a-103">Azure SQL veritabanının denetleme ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83e2a-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="83e2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83e2a-104">SYNTAX</span></span>

### <span data-ttu-id="83e2a-105">DatabaseParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83e2a-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e2a-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83e2a-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e2a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83e2a-107">DESCRIPTION</span></span>
<span data-ttu-id="83e2a-108">**Remove-AzSqlDatabaseAudit** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83e2a-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="83e2a-109">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="83e2a-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="83e2a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83e2a-110">EXAMPLES</span></span>

### <span data-ttu-id="83e2a-111">Örnek 1: Azure SQL veritabanının denetleme ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="83e2a-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="83e2a-112">Örnek 2: Azure SQL veritabanının denetim ayarlarını ardışık düzen aracılığıyla kaldırma</span><span class="sxs-lookup"><span data-stu-id="83e2a-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="83e2a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83e2a-113">PARAMETERS</span></span>

### <span data-ttu-id="83e2a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83e2a-114">-DatabaseName</span></span>
<span data-ttu-id="83e2a-115">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="83e2a-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e2a-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="83e2a-116">-DatabaseObject</span></span>
<span data-ttu-id="83e2a-117">Denetim ilkesini yönetmek için veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="83e2a-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e2a-118">-DefaultProfile</span></span>
<span data-ttu-id="83e2a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83e2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e2a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e2a-120">-ResourceGroupName</span></span>
<span data-ttu-id="83e2a-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="83e2a-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e2a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83e2a-122">-ServerName</span></span>
<span data-ttu-id="83e2a-123">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="83e2a-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e2a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="83e2a-124">-Confirm</span></span>
<span data-ttu-id="83e2a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83e2a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e2a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e2a-126">-WhatIf</span></span>
<span data-ttu-id="83e2a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83e2a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83e2a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83e2a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e2a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e2a-129">CommonParameters</span></span>
<span data-ttu-id="83e2a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83e2a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e2a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83e2a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e2a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83e2a-132">INPUTS</span></span>

### <span data-ttu-id="83e2a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83e2a-133">System.String</span></span>

### <span data-ttu-id="83e2a-134">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="83e2a-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="83e2a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83e2a-135">OUTPUTS</span></span>

### <span data-ttu-id="83e2a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83e2a-136">System.Boolean</span></span>

## <span data-ttu-id="83e2a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83e2a-137">NOTES</span></span>

## <span data-ttu-id="83e2a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83e2a-138">RELATED LINKS</span></span>