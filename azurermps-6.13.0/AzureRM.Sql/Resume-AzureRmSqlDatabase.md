---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590822"
---
# <span data-ttu-id="8df59-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="8df59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df59-102">SYNOPSIS</span></span>
<span data-ttu-id="8df59-103">SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8df59-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8df59-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8df59-105">DESCRIPTION</span></span>
<span data-ttu-id="8df59-106">**Özgeçmiş-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8df59-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8df59-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8df59-107">EXAMPLES</span></span>

### <span data-ttu-id="8df59-108">Örnek 1: Azure SQL veri ambarı veritabanını sürdürür</span><span class="sxs-lookup"><span data-stu-id="8df59-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8df59-109">Bu komut, askıya alınmış Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="8df59-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8df59-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8df59-110">PARAMETERS</span></span>

### <span data-ttu-id="8df59-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="8df59-111">-AsJob</span></span>
<span data-ttu-id="8df59-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8df59-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8df59-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8df59-113">-DatabaseName</span></span>
<span data-ttu-id="8df59-114">Bu cmdlet 'in geri aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8df59-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="8df59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df59-115">-DefaultProfile</span></span>
<span data-ttu-id="8df59-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8df59-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8df59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df59-117">-ResourceGroupName</span></span>
<span data-ttu-id="8df59-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8df59-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8df59-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8df59-119">-ServerName</span></span>
<span data-ttu-id="8df59-120">Bu cmdlet 'in geri aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8df59-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="8df59-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="8df59-121">-Confirm</span></span>
<span data-ttu-id="8df59-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8df59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df59-123">-WhatIf</span></span>
<span data-ttu-id="8df59-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8df59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df59-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8df59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df59-126">CommonParameters</span></span>
<span data-ttu-id="8df59-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8df59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df59-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df59-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df59-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8df59-129">INPUTS</span></span>

### <span data-ttu-id="8df59-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8df59-130">System.String</span></span>

## <span data-ttu-id="8df59-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8df59-131">OUTPUTS</span></span>

### <span data-ttu-id="8df59-132">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="8df59-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8df59-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8df59-133">NOTES</span></span>
* <span data-ttu-id="8df59-134">**Özgeçmiş-AzureRmSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="8df59-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="8df59-135">Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="8df59-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="8df59-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8df59-136">RELATED LINKS</span></span>

[<span data-ttu-id="8df59-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="8df59-138">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="8df59-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="8df59-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="8df59-141">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8df59-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="8df59-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="8df59-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


