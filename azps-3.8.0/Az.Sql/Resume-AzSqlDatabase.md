---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096354"
---
# <span data-ttu-id="8dc66-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="8dc66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc66-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc66-103">SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8dc66-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8dc66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dc66-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dc66-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc66-106">**Özgeçmiş-AzSqlDatabase** cmdlet 'ı Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8dc66-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8dc66-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dc66-107">EXAMPLES</span></span>

### <span data-ttu-id="8dc66-108">Örnek 1: Azure SQL veri ambarı veritabanını sürdürür</span><span class="sxs-lookup"><span data-stu-id="8dc66-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8dc66-109">Bu komut, askıya alınmış Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8dc66-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8dc66-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dc66-110">PARAMETERS</span></span>

### <span data-ttu-id="8dc66-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="8dc66-111">-AsJob</span></span>
<span data-ttu-id="8dc66-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8dc66-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc66-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dc66-113">-DatabaseName</span></span>
<span data-ttu-id="8dc66-114">Bu cmdlet 'in geri aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="8dc66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc66-115">-DefaultProfile</span></span>
<span data-ttu-id="8dc66-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8dc66-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dc66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc66-117">-ResourceGroupName</span></span>
<span data-ttu-id="8dc66-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8dc66-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8dc66-119">-ServerName</span></span>
<span data-ttu-id="8dc66-120">Bu cmdlet 'in geri aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="8dc66-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="8dc66-121">-Confirm</span></span>
<span data-ttu-id="8dc66-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8dc66-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc66-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc66-123">-WhatIf</span></span>
<span data-ttu-id="8dc66-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc66-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc66-126">CommonParameters</span></span>
<span data-ttu-id="8dc66-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dc66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc66-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8dc66-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc66-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dc66-129">INPUTS</span></span>

### <span data-ttu-id="8dc66-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8dc66-130">System.String</span></span>

## <span data-ttu-id="8dc66-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dc66-131">OUTPUTS</span></span>

### <span data-ttu-id="8dc66-132">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="8dc66-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8dc66-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dc66-133">NOTES</span></span>
* <span data-ttu-id="8dc66-134">**Resume-AzSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="8dc66-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="8dc66-135">Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="8dc66-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="8dc66-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dc66-136">RELATED LINKS</span></span>

[<span data-ttu-id="8dc66-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8dc66-138">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8dc66-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8dc66-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8dc66-141">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8dc66-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8dc66-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="8dc66-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

