---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594986"
---
# <span data-ttu-id="f076e-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f076e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f076e-102">SYNOPSIS</span></span>
<span data-ttu-id="f076e-103">SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="f076e-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f076e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f076e-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f076e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f076e-105">DESCRIPTION</span></span>
<span data-ttu-id="f076e-106">**Özgeçmiş-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="f076e-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f076e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f076e-107">EXAMPLES</span></span>

### <span data-ttu-id="f076e-108">Örnek 1: Azure SQL veri ambarı veritabanını sürdürür</span><span class="sxs-lookup"><span data-stu-id="f076e-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f076e-109">Bu komut, askıya alınmış Azure SQL veri ambarı veritabanını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="f076e-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f076e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f076e-110">PARAMETERS</span></span>

### <span data-ttu-id="f076e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f076e-111">-DatabaseName</span></span>
<span data-ttu-id="f076e-112">Bu cmdlet 'in geri aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f076e-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="f076e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f076e-113">-ResourceGroupName</span></span>
<span data-ttu-id="f076e-114">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f076e-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f076e-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f076e-115">-ServerName</span></span>
<span data-ttu-id="f076e-116">Bu cmdlet 'in geri aldığı veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f076e-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="f076e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f076e-117">-Confirm</span></span>
<span data-ttu-id="f076e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f076e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f076e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f076e-119">-WhatIf</span></span>
<span data-ttu-id="f076e-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f076e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f076e-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f076e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f076e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f076e-122">-DefaultProfile</span></span>
<span data-ttu-id="f076e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f076e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f076e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f076e-124">CommonParameters</span></span>
<span data-ttu-id="f076e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f076e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f076e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f076e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f076e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f076e-127">INPUTS</span></span>

### <span data-ttu-id="f076e-128">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="f076e-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f076e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f076e-129">OUTPUTS</span></span>

### <span data-ttu-id="f076e-130">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="f076e-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f076e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f076e-131">NOTES</span></span>
* <span data-ttu-id="f076e-132">**Özgeçmiş-AzureRmSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="f076e-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="f076e-133">Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="f076e-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="f076e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f076e-134">RELATED LINKS</span></span>

[<span data-ttu-id="f076e-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f076e-136">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f076e-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f076e-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f076e-139">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f076e-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f076e-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f076e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


