---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098672"
---
# <span data-ttu-id="2faa9-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2faa9-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="2faa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2faa9-102">SYNOPSIS</span></span>
<span data-ttu-id="2faa9-103">SQL veritabanıyla belirtilen ikincil veritabanı arasında veri çoğaltmayı sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="2faa9-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="2faa9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2faa9-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2faa9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2faa9-105">DESCRIPTION</span></span>
<span data-ttu-id="2faa9-106">**Remove-AzSqlDatabaseSecondary** cmdlet 'i coğrafi çoğaltma bağlantısını sonlandırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2faa9-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="2faa9-107">Bu cmdlet Stop-AzSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="2faa9-108">İşten çıkmadan önce çoğaltma eşitlemesi yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="2faa9-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="2faa9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2faa9-109">EXAMPLES</span></span>

## <span data-ttu-id="2faa9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2faa9-110">PARAMETERS</span></span>

### <span data-ttu-id="2faa9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2faa9-111">-DatabaseName</span></span>
<span data-ttu-id="2faa9-112">Bu cmdlet 'in kaldırıldığı çoğaltma bağlantısının bulunduğu birincil Azure SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2faa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2faa9-113">-DefaultProfile</span></span>
<span data-ttu-id="2faa9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2faa9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2faa9-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faa9-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2faa9-116">İş ortağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2faa9-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2faa9-117">-PartnerServerName</span></span>
<span data-ttu-id="2faa9-118">İş ortağı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2faa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="2faa9-120">Kaldırılacak olan çoğaltma bağlantısıyla ilişkilendirilmiş olan kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="2faa9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2faa9-121">-ServerName</span></span>
<span data-ttu-id="2faa9-122">Kaldırılacak çoğaltma bağlantısının bulunduğu SQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="2faa9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2faa9-123">-Confirm</span></span>
<span data-ttu-id="2faa9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2faa9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2faa9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2faa9-125">-WhatIf</span></span>
<span data-ttu-id="2faa9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2faa9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2faa9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2faa9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2faa9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2faa9-128">CommonParameters</span></span>
<span data-ttu-id="2faa9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2faa9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2faa9-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2faa9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2faa9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2faa9-131">INPUTS</span></span>

### <span data-ttu-id="2faa9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2faa9-132">System.String</span></span>

## <span data-ttu-id="2faa9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2faa9-133">OUTPUTS</span></span>

### <span data-ttu-id="2faa9-134">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="2faa9-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="2faa9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2faa9-135">NOTES</span></span>

## <span data-ttu-id="2faa9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2faa9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2faa9-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2faa9-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="2faa9-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2faa9-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="2faa9-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="2faa9-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
